---
description: 'Дополнительные сведения о: Крецентфилелист Class'
title: Класс Крецентфилелист
ms.date: 11/04/2016
f1_keywords:
- CRecentFileList
- AFXADV/CRecentFileList
- AFXADV/CRecentFileList::CRecentFileList
- AFXADV/CRecentFileList::Add
- AFXADV/CRecentFileList::GetDisplayName
- AFXADV/CRecentFileList::GetSize
- AFXADV/CRecentFileList::ReadList
- AFXADV/CRecentFileList::Remove
- AFXADV/CRecentFileList::UpdateMenu
- AFXADV/CRecentFileList::WriteList
helpviewer_keywords:
- CRecentFileList [MFC], CRecentFileList
- CRecentFileList [MFC], Add
- CRecentFileList [MFC], GetDisplayName
- CRecentFileList [MFC], GetSize
- CRecentFileList [MFC], ReadList
- CRecentFileList [MFC], Remove
- CRecentFileList [MFC], UpdateMenu
- CRecentFileList [MFC], WriteList
ms.assetid: a77f0524-7584-4582-849a-7e97b76d186e
ms.openlocfilehash: 9433e65336cba1018c7bff8cf3a90e239ae5e3eb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97301130"
---
# <a name="crecentfilelist-class"></a>Класс Крецентфилелист

Поддерживает элемент управления последнего использовавшегося списка файлов (MRU).

## <a name="syntax"></a>Синтаксис

```
class CRecentFileList
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Крецентфилелист:: Крецентфилелист](#crecentfilelist)|Формирует объект `CRecentFileList`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Крецентфилелист:: Add](#add)|Добавляет файл в список файлов MRU.|
|[Крецентфилелист::/DisplayName](#getdisplayname)|Предоставляет отображаемое имя для вывода меню имени файла MRU.|
|[Крецентфилелист:: DataSize](#getsize)|Возвращает количество файлов в списке MRU.|
|[Крецентфилелист:: ReadList](#readlist)|Считывает список последних файлов из реестра или. INI-файл.|
|[Крецентфилелист:: Remove](#remove)|Удаляет файл из списка MRU-файлов.|
|[Крецентфилелист:: Упдатемену](#updatemenu)|Обновляет отображение списка файлов MRU.|
|[Крецентфилелист:: Врителист](#writelist)|Записывает список MRU файлов из реестра или. INI-файл.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Крецентфилелист:: operator \[\]](#operator_at)|Возвращает `CString` объект в заданной позиции.|

## <a name="remarks"></a>Комментарии

Файлы можно добавлять в список файлов MRU или удалять из него, список файлов можно считывать из реестра или записывать в него. INI-файл, и меню, в котором отображается список файлов MRU, можно обновить.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CRecentFileList`

## <a name="requirements"></a>Требования

**Заголовок:** афксадв. h

## <a name="crecentfilelistadd"></a><a name="add"></a> Крецентфилелист:: Add

Добавляет файл в список последних использованных файлов (MRU).

```
virtual void Add(LPCTSTR lpszPathName);

virtual void Add(
    LPCTSTR lpszPathName,
    LPCTSTR lpszAppID);

void Add(
    IShellItem* pItem,
    LPCTSTR lpszAppID);

void Add(
    IShellLink* pLink,
    LPCTSTR lpszAppID);

void Add(
    PIDLIST_ABSOLUTE pidl,
    LPCTSTR lpszAppID);
```

### <a name="parameters"></a>Параметры

*лпсзпаснаме*<br/>
Указывает путь для добавления в список.

*лпсзаппид*<br/>
Указывает идентификатор модели пользователя приложения.

*питем*<br/>
Указывает указатель на элемент оболочки, добавляемый в список.

*плинк*<br/>
Указывает указатель на ссылку на оболочку, добавляемую в список.

*пидл*<br/>
Указывает IDLIST для элемента оболочки, который должен быть добавлен в папку последних документов.

### <a name="remarks"></a>Комментарии

Имя файла будет добавлено в верхнюю часть списка MRU. Если имя файла уже существует в списке MRU, оно будет перемещено в начало.

## <a name="crecentfilelistcrecentfilelist"></a><a name="crecentfilelist"></a> Крецентфилелист:: Крецентфилелист

Формирует объект `CRecentFileList`.

```
CRecentFileList(
    UINT nStart,
    LPCTSTR lpszSection,
    LPCTSTR lpszEntryFormat,
    int nSize,
    int nMaxDispLen = AFX_ABBREV_FILENAME_LEN);
```

### <a name="parameters"></a>Параметры

*нстарт*<br/>
Смещение для нумерации в меню, отображаемом в списке последних использовавшихся файлов.

*лпсзсектион*<br/>
Указывает на имя раздела реестра или приложения. INI-файл, в который считывается и/или записывается список файлов MRU.

*лпсзентриформат*<br/>
Указывает на строку формата, используемую для имен записей, хранящихся в реестре или в приложении. INI-файл.

*нсизе*<br/>
Максимальное число файлов в списке файлов MRU.

*нмаксдисплен*<br/>
Максимальная длина в символах, доступная в меню для вывода имени файла в списке MRU-файлов.

### <a name="remarks"></a>Комментарии

Строка формата, на которую указывает *лпсзентриформат* , должна содержать "% d", который будет использоваться для замены индекса каждого элемента MRU. Например, если строка формата, `"file%d"` то записи будут называться `file0` , `file1` и т. д.

## <a name="crecentfilelistgetdisplayname"></a><a name="getdisplayname"></a> Крецентфилелист::/DisplayName

Получает отображаемое имя для файла из списка MRU-файлов для использования в меню, отображаемом в списке MRU.

```
virtual BOOL GetDisplayName(
    CString& strName,
    int nIndex,
    LPCTSTR lpszCurDir,
    int nCurDir,
    BOOL bAtLeastName = TRUE) const;
```

### <a name="parameters"></a>Параметры

*strName*<br/>
Полный путь к файлу, имя которого должно отображаться в списке MRU-файлов.

*ниндекс*<br/>
Отсчитываемый от нуля индекс файла в списке MRU-файлов.

*лпсзкурдир*<br/>
Строка, содержащая текущий каталог.

*нкурдир*<br/>
Длина текущей строки каталога.

*батлеастнаме*<br/>
Если значение не равно нулю, указывает, что должно возвращаться базовое имя файла, даже если оно превышает максимальную длину (передается в качестве параметра *нмаксдисплен* в `CRecentFileList` конструктор).

### <a name="return-value"></a>Возвращаемое значение

**Значение false** , если в списке последних использованных файлов отсутствует имя файла по указанному индексу.

### <a name="remarks"></a>Комментарии

Если файл находится в текущем каталоге, функция оставляет каталог за пределами экрана. Если имя файла слишком длинное, то каталог и расширение удаляются. Если имя файла по-прежнему слишком длинное, отображаемое имя задается пустой строкой, если только *батлеастнаме* не имеет ненулевого значения.

## <a name="crecentfilelistgetsize"></a><a name="getsize"></a> Крецентфилелист:: DataSize

Возвращает количество файлов в списке MRU.

```
int GetSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число файлов в текущем списке недавно использованных файлов (MRU).

## <a name="crecentfilelistoperator--"></a><a name="operator_at"></a> Крецентфилелист:: operator []

Перегруженный `[]` оператор index () возвращает значение типа Single, `CString` заданное с помощью индекса, начинающегося с нуля, в *ниндекс*.

```
CString& operator[ ](int nindex);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Отсчитываемый от нуля индекс объекта `CString` в наборе `CString` s.

## <a name="crecentfilelistreadlist"></a><a name="readlist"></a> Крецентфилелист:: ReadList

Считывает список последних использованных файлов (MRU) из реестра или приложения. INI-файл.

```
virtual void ReadList();
```

## <a name="crecentfilelistremove"></a><a name="remove"></a> Крецентфилелист:: Remove

Удаляет файл из списка MRU-файлов.

```
virtual void Remove(int nIndex);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Отсчитываемый от нуля индекс файла, который должен быть удален из списка недавно использованных файлов (MRU).

## <a name="crecentfilelistupdatemenu"></a><a name="updatemenu"></a> Крецентфилелист:: Упдатемену

Обновляет отображение списка файлов MRU.

```
virtual void UpdateMenu(CCmdUI* pCmdUI);
```

### <a name="parameters"></a>Параметры

*пкмдуи*<br/>
Указатель на объект [Поддержка CCmdUI](../../mfc/reference/ccmdui-class.md) для последнего использованного меню списка файлов (MRU).

## <a name="crecentfilelistwritelist"></a><a name="writelist"></a> Крецентфилелист:: Врителист

Записывает список последних использованных файлов (MRU) в реестр или приложение. INI-файл.

```
virtual void WriteList();
```

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
