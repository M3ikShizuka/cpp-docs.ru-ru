---
description: 'Дополнительные сведения о: Ккустомвиндовсфиле'
title: CCustomWindowsFile
ms.date: 10/22/2018
f1_keywords:
- cmyproviderwindowsfile
- ccustomwindowsfile
helpviewer_keywords:
- CMyProviderWindowsFile class
- OLE DB providers, wizard-generated files
- CCustomWindowsFile class
ms.assetid: 0e9e72ac-1e1e-445f-a7ac-690c20031f9d
ms.openlocfilehash: c0df2840b68a350f9d65102fdf0a962681edefd9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170403"
---
# <a name="ccustomwindowsfile"></a>CCustomWindowsFile

Мастер создает класс с одной строкой данных. в этом случае он называется `CCustomWindowsFile` . Следующий код для `CCustomWindowsFile` мастера создан и перечисляет все файлы в каталоге с помощью `WIN32_FIND_DATA` структуры. `CCustomWindowsFile` наследует от `WIN32_FIND_DATA` структуры:

```cpp
/////////////////////////////////////////////////////////////////////
// CustomRS.H

class CCustomWindowsFile:
   public WIN32_FIND_DATA
{
public:
BEGIN_PROVIDER_COLUMN_MAP(CCustomWindowsFile)
   PROVIDER_COLUMN_ENTRY("FileAttributes", 1, dwFileAttributes)
   PROVIDER_COLUMN_ENTRY("FileSizeHigh", 2, nFileSizeHigh)
   PROVIDER_COLUMN_ENTRY("FileSizeLow", 3, nFileSizeLow)
   PROVIDER_COLUMN_ENTRY_STR("FileName", 4, cFileName)
   PROVIDER_COLUMN_ENTRY_STR("AltFileName", 5, cAlternateFileName)
END_PROVIDER_COLUMN_MAP()
};
```

`CCustomWindowsFile` метод называется [классом записей пользователя](../../data/oledb/user-record.md) , так как он также содержит карту, описывающую столбцы в наборе строк поставщика. Таблица столбцов поставщика содержит одну запись для каждого поля в наборе строк с помощью макросов PROVIDER_COLUMN_ENTRY. Макросы указывают имя столбца, порядковый номер и смещение для записи структуры. Записи столбцов поставщика в приведенном выше коде содержат смещения в `WIN32_FIND_DATA` структуре. Когда потребитель вызывает `IRowset::GetData` , данные передаются в один непрерывный буфер. Вместо того чтобы выполнять вычисления с помощью указателей, на карте можно указать элемент данных.

`CCustomRowset`Класс также содержит `Execute` метод. `Execute` фактически считывает данные из собственного источника. В следующем коде показан метод, созданный мастером `Execute` . Функция использует Win32 `FindFirstFile` и `FindNextFile` API для получения сведений о файлах в каталоге и помещает их в экземпляры `CCustomWindowsFile` класса.

```cpp
/////////////////////////////////////////////////////////////////////
// CustomRS.H

HRESULT Execute(DBPARAMS * pParams, LONG* pcRowsAffected)
{
   USES_CONVERSION;
   BOOL bFound = FALSE;
   HANDLE hFile;
   LPTSTR  szDir = (m_strCommandText == _T("")) ? _T("*.*") :
       OLE2T(m_strCommandText);
   CCustomWindowsFile wf;
   hFile = FindFirstFile(szDir, &wf);
   if (hFile == INVALID_HANDLE_VALUE)
      return DB_E_ERRORSINCOMMAND;
   LONG cFiles = 1;
   BOOL bMoreFiles = TRUE;
   while (bMoreFiles)
   {
      if (!m_rgRowData.Add(wf))
         return E_OUTOFMEMORY;
      bMoreFiles = FindNextFile(hFile, &wf);
      cFiles++;
   }
   FindClose(hFile);
   if (pcRowsAffected != NULL)
      *pcRowsAffected = cFiles;
   return S_OK;
}
```

Каталог для поиска отображается `m_strCommandText` ; он содержит текст, представленный `ICommandText` интерфейсом в объекте Command. Если каталог не указан, используется текущий каталог.

Метод создает одну запись для каждого файла (соответствующего строке) и помещает ее в `m_rgRowData` элемент данных. `CRowsetImpl`Класс определяет `m_rgRowData` элемент данных. Данные в этом массиве показаны для всей таблицы и используются во всех шаблонах.

## <a name="see-also"></a>См. также раздел

[Файлы Wizard-Generated поставщика](../../data/oledb/provider-wizard-generated-files.md)<br/>
