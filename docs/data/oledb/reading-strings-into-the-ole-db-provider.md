---
description: 'Дополнительные сведения: считывание строк в поставщик OLE DB'
title: Чтение строк в поставщике OLE DB
ms.date: 10/13/2018
helpviewer_keywords:
- OLE DB providers, reading strings into
ms.assetid: 517f322c-f37e-4eed-bf5e-dd9a412c2f98
ms.openlocfilehash: 5df8812d5589dd457684bf5e36a8a49f798f99aa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286635"
---
# <a name="reading-strings-into-the-ole-db-provider"></a>Чтение строк в поставщике OLE DB

`CCustomRowset::Execute`Функция открывает файл и считывает строки. Потребитель передает имя файла поставщику, вызывая [ICommandText:: SetCommandText](/previous-versions/windows/desktop/ms709757(v=vs.85)). Поставщик получает имя файла и сохраняет его в переменной члена `m_strCommandText` . `Execute` считывает имя файла из `m_strCommandText` . Если имя файла является недопустимым или файл недоступен, `Execute` возвращает ошибку. В противном случае он открывает файл и вызовы `fgets` для получения строк. Для каждого набора строк, которые он считывает, `Execute` создает экземпляр записи пользователя (измененный `CCustomWindowsFile` из [хранения строк в поставщике OLE DB](../../data/oledb/storing-strings-in-the-ole-db-provider.md)) и помещает его в массив.

Если файл не может быть открыт, `Execute` должен возвращаться DB_E_NOTABLE. Если вместо этого он возвращает E_FAIL, поставщик не будет работать с множеством потребителей и не будет передавать [тесты на соответствие](../../data/oledb/testing-your-provider.md)OLE DB.

## <a name="example"></a>Пример

```cpp
/////////////////////////////////////////////////////////////////////////
// CustomRS.h
class CCustomRowset : public CRowsetImpl< CCustomRowset, CCustomWindowsFile, CCustomCommand>
{
public:
    HRESULT Execute(DBPARAMS * pParams, LONG* pcRowsAffected)
    {
        enum {
            sizeOfBuffer = 256,
            sizeOfFile = MAX_PATH
        };
        USES_CONVERSION;
        FILE* pFile = NULL;
        TCHAR szString[sizeOfBuffer];
        TCHAR szFile[sizeOfFile];
        size_t nLength;

        ObjectLock lock(this);

        // From a filename, passed in as a command text, scan the file
        // placing data in the data array.
        if (!m_strCommandText)
        {
            ATLTRACE("No filename specified");
            return E_FAIL;
        }

        // Open the file
        _tcscpy_s(szFile, sizeOfFile, m_strCommandText);
        if (szFile[0] == _T('\0') ||
            (fopen_s(&pFile, (char*)&szFile[0], "r") == 0))
        {
            ATLTRACE("Could not open file");
            return DB_E_NOTABLE;
        }

        // Scan and parse the file.
        // The file should contain two strings per record
        LONG cFiles = 0;
        while (fgets((char*)szString, sizeOfBuffer, pFile) != NULL)
        {
            nLength = strnlen((char*)szString, sizeOfBuffer);
            szString[nLength-1] = '\0';   // Strip off trailing CR/LF
            CCustomWindowsFile am;
            _tcscpy_s(am.szCommand, am.iSize, szString);
            _tcscpy_s(am.szCommand2, am.iSize, szString);

            if (fgets((char*)szString, sizeOfBuffer, pFile) != NULL)
            {
                nLength = strnlen((char*)szString, sizeOfBuffer);
                szString[nLength-1] = '\0'; // Strip off trailing CR/LF
                _tcscpy_s(am.szText, am.iSize, szString);
                _tcscpy_s(am.szText2, am.iSize, szString);
            }

            am.dwBookmark = ++cFiles;
            if (!m_rgRowData.Add(am))
            {
                ATLTRACE("Couldn't add data to array");
                fclose(pFile);
                return E_FAIL;
            }
        }

        if (pcRowsAffected != NULL)
            *pcRowsAffected = cFiles;
        return S_OK;
    }
};
```

Когда это будет сделано, поставщик должен быть готов к компиляции и выполнению. Для тестирования поставщика необходим потребитель с соответствующей функциональностью. [Реализация простого потребителя](../../data/oledb/implementing-a-simple-consumer.md) демонстрирует создание такого тестового потребителя. Запустите тестового потребителя с поставщиком и убедитесь, что тестовый потребитель получает соответствующие строки от поставщика.

После успешного тестирования поставщика может потребоваться повысить его функциональность путем реализации дополнительных интерфейсов. Пример показан в [усовершенствовании простого поставщика Read-Only](../../data/oledb/enhancing-the-simple-read-only-provider.md).

## <a name="see-also"></a>См. также раздел

[Реализация простого поставщика Read-Only](../../data/oledb/implementing-the-simple-read-only-provider.md)<br/>
