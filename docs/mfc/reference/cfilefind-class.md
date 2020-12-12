---
description: 'Дополнительные сведения о: Кфилефинд Class'
title: Класс Кфилефинд
ms.date: 11/04/2016
f1_keywords:
- CFileFind
- AFX/CFileFind
- AFX/CFileFind::CFileFind
- AFX/CFileFind::Close
- AFX/CFileFind::FindFile
- AFX/CFileFind::FindNextFile
- AFX/CFileFind::GetCreationTime
- AFX/CFileFind::GetFileName
- AFX/CFileFind::GetFilePath
- AFX/CFileFind::GetFileTitle
- AFX/CFileFind::GetFileURL
- AFX/CFileFind::GetLastAccessTime
- AFX/CFileFind::GetLastWriteTime
- AFX/CFileFind::GetLength
- AFX/CFileFind::GetRoot
- AFX/CFileFind::IsArchived
- AFX/CFileFind::IsCompressed
- AFX/CFileFind::IsDirectory
- AFX/CFileFind::IsDots
- AFX/CFileFind::IsHidden
- AFX/CFileFind::IsNormal
- AFX/CFileFind::IsReadOnly
- AFX/CFileFind::IsSystem
- AFX/CFileFind::IsTemporary
- AFX/CFileFind::MatchesMask
- AFX/CFileFind::CloseContext
- AFX/CFileFind::m_pTM
helpviewer_keywords:
- CFileFind [MFC], CFileFind
- CFileFind [MFC], Close
- CFileFind [MFC], FindFile
- CFileFind [MFC], FindNextFile
- CFileFind [MFC], GetCreationTime
- CFileFind [MFC], GetFileName
- CFileFind [MFC], GetFilePath
- CFileFind [MFC], GetFileTitle
- CFileFind [MFC], GetFileURL
- CFileFind [MFC], GetLastAccessTime
- CFileFind [MFC], GetLastWriteTime
- CFileFind [MFC], GetLength
- CFileFind [MFC], GetRoot
- CFileFind [MFC], IsArchived
- CFileFind [MFC], IsCompressed
- CFileFind [MFC], IsDirectory
- CFileFind [MFC], IsDots
- CFileFind [MFC], IsHidden
- CFileFind [MFC], IsNormal
- CFileFind [MFC], IsReadOnly
- CFileFind [MFC], IsSystem
- CFileFind [MFC], IsTemporary
- CFileFind [MFC], MatchesMask
- CFileFind [MFC], CloseContext
- CFileFind [MFC], m_pTM
ms.assetid: 9990068c-b023-4114-9580-a50182d15240
ms.openlocfilehash: d47c45ac86386a6748ca212c569aeef568ca2a8a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97184508"
---
# <a name="cfilefind-class"></a>Класс Кфилефинд

Выполняет поиск по локальному файлу и является базовым классом для [кгоферфилефинд](../../mfc/reference/cgopherfilefind-class.md) и [кфтпфилефинд](../../mfc/reference/cftpfilefind-class.md), которые выполняют поиск файлов в Интернете.

## <a name="syntax"></a>Синтаксис

```
class CFileFind : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кфилефинд:: Кфилефинд](#cfilefind)|Формирует объект `CFileFind`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кфилефинд:: Close](#close)|Закрывает поисковый запрос.|
|[Кфилефинд:: Финдфиле](#findfile)|Выполняет поиск указанного имени файла в каталоге.|
|[Кфилефинд:: FindNextFile](#findnextfile)|Возобновляет Поиск файла из предыдущего вызова [финдфиле](#findfile).|
|[Кфилефинд:: Жеткреатионтиме](#getcreationtime)|Возвращает время создания файла.|
|[Кфилефинд:: имя_файла](#getfilename)|Возвращает имя найденного файла, включая расширение.|
|[Кфилефинд:: FilePath](#getfilepath)|Возвращает полный путь к найденному файлу.|
|[Кфилефинд:: Жетфилетитле](#getfiletitle)|Возвращает заголовок найденного файла. Заголовок не включает расширение.|
|[Кфилефинд:: Жетфилеурл](#getfileurl)|Возвращает URL-адрес найденного файла, включая путь к файлу.|
|[Кфилефинд:: Жетластакцесстиме](#getlastaccesstime)|Возвращает время последнего обращения к файлу.|
|[Кфилефинд:: Жетластвритетиме](#getlastwritetime)|Возвращает время последнего изменения и сохранения файла.|
|[Кфилефинд:: DATALENGTH](#getlength)|Возвращает длину найденного файла в байтах.|
|[Кфилефинд:: root](#getroot)|Возвращает корневой каталог найденного файла.|
|[Кфилефинд:: Archive](#isarchived)|Определяет, архивируется ли найденный файл.|
|[Кфилефинд:: уплотнение](#iscompressed)|Определяет, сжат ли найденный файл.|
|[Кфилефинд:: подкаталог](#isdirectory)|Определяет, является ли найденный файл каталогом.|
|[Кфилефинд:: наТочки](#isdots)|Определяет, имеет ли имя найденного файла имя "." или "..", указывая, что фактически является каталогом.|
|[Кфилефинд:: Hidden](#ishidden)|Определяет, скрыт ли найденный файл.|
|[Кфилефинд:: onобычная](#isnormal)|Определяет, является ли найденный файл нормальным (иными словами, не имеет других атрибутов).|
|[Кфилефинд:: IsReadOnly](#isreadonly)|Определяет, доступен ли найденный файл только для чтения.|
|[Кфилефинд:: a System](#issystem)|Определяет, является ли найденный файл системным.|
|[Кфилефинд::](#istemporary)|Определяет, является ли найденный файл временным.|
|[Кфилефинд:: Матчесмаск](#matchesmask)|Указывает необходимые атрибуты файла для поиска.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кфилефинд:: Клосеконтекст](#closecontext)|Закрывает файл, указанный текущим поисковым маркером.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Кфилефинд:: m_pTM](#m_ptm)|Указатель на `CAtlTransactionManager` объект.|

## <a name="remarks"></a>Комментарии

`CFileFind` включает функции-члены, которые начинают поиск, находят файл и возвращают заголовок, имя или путь к файлу. При поиске в Интернете функция-член [жетфилеурл](#getfileurl) возвращает URL файла.

`CFileFind` является базовым классом для двух других классов MFC, предназначенных для поиска конкретных типов серверов: `CGopherFileFind` работает специально с серверами Gopher и `CFtpFileFind` работает специально с FTP-серверами. Вместе эти три класса предоставляют клиенту простой механизм поиска файлов независимо от протокола сервера, типа файла или расположения на локальном или удаленном сервере.

Следующий код выполнит перечисление всех файлов в текущем каталоге, выполнив печать имени каждого файла:

[!code-cpp[NVC_MFCFiles#31](../../atl-mfc-shared/reference/codesnippet/cpp/cfilefind-class_1.cpp)]

Чтобы упростить этот пример, в этом коде используется класс стандартной библиотеки C++ `cout` . `cout`Строку можно заменить на вызов `CListBox::AddString` , например, в программе с графическим пользовательским интерфейсом.

Дополнительные сведения об использовании `CFileFind` и других классах WinInet см. в статье [Интернет – программирование с помощью WinInet](../../mfc/win32-internet-extensions-wininet.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CFileFind`

## <a name="requirements"></a>Требования

**Заголовок:** AFX. h

## <a name="cfilefindcfilefind"></a><a name="cfilefind"></a> Кфилефинд:: Кфилефинд

Эта функция-член вызывается при `CFileFind` создании объекта.

```
CFileFind();
CFileFind(CAtlTransactionManager* pTM);
```

### <a name="parameters"></a>Параметры

*pTM*<br/>
Указатель на объект CAtlTransactionManager.

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: filename](#getfilename).

## <a name="cfilefindclose"></a><a name="close"></a> Кфилефинд:: Close

Вызовите эту функцию члена, чтобы завершить поиск, сбросить контекст и освободить все ресурсы.

```cpp
void Close();
```

### <a name="remarks"></a>Комментарии

После вызова `Close` не нужно создавать новый `CFileFind` экземпляр перед вызовом [финдфиле](#findfile) , чтобы начать новый поиск.

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: filename](#getfilename).

## <a name="cfilefindclosecontext"></a><a name="closecontext"></a> Кфилефинд:: Клосеконтекст

Закрывает файл, указанный текущим поисковым маркером.

```
virtual void CloseContext();
```

### <a name="remarks"></a>Комментарии

Закрывает файл, заданный текущим значением маркера поиска. Переопределите эту функцию, чтобы изменить поведение по умолчанию.

Чтобы получить допустимый маркер поиска, необходимо вызвать функции [финдфиле](#findfile) или [FindNextFile](#findnextfile) по крайней мере один раз. `FindFile`Функции и `FindNextFile` используют описатель поиска для поиска файлов с именами, соответствующими заданному имени.

## <a name="cfilefindfindfile"></a><a name="findfile"></a> Кфилефинд:: Финдфиле

Вызовите эту функцию-член, чтобы открыть Поиск файла.

```
virtual BOOL FindFile(
    LPCTSTR pstrName = NULL,
    DWORD dwUnused = 0);
```

### <a name="parameters"></a>Параметры

*пстрнаме*<br/>
Указатель на строку, содержащую имя искомого файла. Если передать значение NULL для *пстрнаме*, `FindFile` выполняет поиск по подстановочному знаку (*. \* ).

*двунусед*<br/>
Зарезервировано для выполнения `FindFile` полиморфизма с производными классами. Должно быть равно 0.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0. Чтобы получить расширенные сведения об ошибке, вызовите функцию Win32 [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

### <a name="remarks"></a>Комментарии

После вызова `FindFile` для начала поиска файла вызовите [FindNextFile](#findnextfile) для получения последующих файлов. Необходимо вызвать `FindNextFile` хотя бы один раз перед вызовом любой из следующих функций члена атрибута:

- [GetCreationTime](#getcreationtime)

- [GetFileName](#getfilename)

- [жетфилетитле](#getfiletitle)

- [Путь к файлу](#getfilepath)

- [жетфилеурл](#getfileurl)

- [жетластакцесстиме](#getlastaccesstime)

- [жетластвритетиме](#getlastwritetime)

- [GetLength](#getlength)

- [GetRoot](#getroot)

- [С заархивированным](#isarchived)

- [IsCompressed](#iscompressed)

- [Подкаталог](#isdirectory)

- [Точки](#isdots)

- [IsHidden](#ishidden)

- [Обычная](#isnormal)

- [IsReadOnly](#isreadonly)

- [IsSystem](#issystem)

- [IsTemporary задано](#istemporary)

- [матчесмаск](#matchesmask)

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DataDirectory](#isdirectory).

## <a name="cfilefindfindnextfile"></a><a name="findnextfile"></a> Кфилефинд:: FindNextFile

Вызовите эту функцию-член, чтобы продолжить поиск файла из предыдущего вызова [финдфиле](#findfile).

```
virtual BOOL FindNextFile();
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если есть больше файлов; нуль, если найденный файл является последним в каталоге или если произошла ошибка. Чтобы получить расширенные сведения об ошибке, вызовите функцию Win32 [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). Если найденный файл является последним файлом в каталоге или не удается найти соответствующие файлы, `GetLastError` функция возвращает ERROR_NO_MORE_FILES.

### <a name="remarks"></a>Комментарии

Необходимо вызвать `FindNextFile` хотя бы один раз перед вызовом любой из следующих функций члена атрибута:

- [GetCreationTime](#getcreationtime)

- [GetFileName](#getfilename)

- [жетфилетитле](#getfiletitle)

- [Путь к файлу](#getfilepath)

- [жетфилеурл](#getfileurl)

- [жетластакцесстиме](#getlastaccesstime)

- [жетластвритетиме](#getlastwritetime)

- [GetLength](#getlength)

- [GetRoot](#getroot)

- [С заархивированным](#isarchived)

- [IsCompressed](#iscompressed)

- [Подкаталог](#isdirectory)

- [Точки](#isdots)

- [IsHidden](#ishidden)

- [Обычная](#isnormal)

- [IsReadOnly](#isreadonly)

- [IsSystem](#issystem)

- [IsTemporary задано](#istemporary)

- [матчесмаск](#matchesmask)

`FindNextFile` заключает в оболочку функцию Win32 [FindNextFile](/windows/win32/api/fileapi/nf-fileapi-findnextfilew).

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DataDirectory](#isdirectory).

## <a name="cfilefindgetcreationtime"></a><a name="getcreationtime"></a> Кфилефинд:: Жеткреатионтиме

Вызовите эту функцию члена, чтобы получить время создания указанного файла.

```
virtual BOOL GetCreationTime(FILETIME* pTimeStamp) const;
virtual BOOL GetCreationTime(CTime& refTime) const;
```

### <a name="parameters"></a>Параметры

*птиместамп*<br/>
Указатель на структуру [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , содержащую время создания файла.

*рефтиме*<br/>
Ссылка на объект [CTime](../../atl-mfc-shared/reference/ctime-class.md) .

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение в случае успешного выполнения; 0 в случае неудачи. `GetCreationTime` Возвращает 0, только если для этого объекта никогда не вызывался [FindNextFile](#findnextfile) `CFileFind` .

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `GetCreationTime` .

> [!NOTE]
> Не все файловые системы используют одну и ту же семантику для реализации отметки времени, возвращаемой этой функцией. Эта функция может возвращать то же значение, что и другие функции отметки времени, если базовая файловая система или сервер не поддерживает поддержание атрибута времени. Сведения о форматах времени см. в разделе Структура [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) . В некоторых операционных системах возвращенное время находится на локальном часовом поясе компьютера, где находится файл. Дополнительные сведения см. в разделе API Win32 [филетиметолокалфилетиме](/windows/win32/api/fileapi/nf-fileapi-filetimetolocalfiletime) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindgetfilename"></a><a name="getfilename"></a> Кфилефинд:: имя_файла

Вызовите эту функцию члена, чтобы получить имя найденного файла.

```
virtual CString GetFileName() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имя самого последнего найденного файла.

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом метода filename.

`GetFileName` является одной из трех `CFileFind` функций-членов, возвращающих некоторую форму имени файла. В следующем списке описаны три и их отличия.

- `GetFileName` Возвращает имя файла, включая расширение. Например, вызов `GetFileName` для создания пользовательского сообщения о файле *c:\myhtml\myfile.txt* возвращает имя файла *myfile.txt*.

- Функция [FilePath](#getfilepath) возвращает полный путь к файлу. Например, вызов `GetFilePath` для создания сообщения пользователя о файле *c:\myhtml\myfile.txt* Возвращает путь к файлу *c:\myhtml\myfile.txt*.

- [Жетфилетитле](#getfiletitle) возвращает имя файла, исключая расширение файла. Например, вызов `GetFileTitle` для создания сообщения пользователя о файле *c:\myhtml\myfile.txt* Возвращает заголовок файла *MyFile*.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCFiles#32](../../atl-mfc-shared/reference/codesnippet/cpp/cfilefind-class_2.cpp)]

## <a name="cfilefindgetfilepath"></a><a name="getfilepath"></a> Кфилефинд:: FilePath

Вызовите эту функцию члена, чтобы получить полный путь к указанному файлу.

```
virtual CString GetFilePath() const;
```

### <a name="return-value"></a>Возвращаемое значение

Путь к указанному файлу.

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `GetFilePath` .

`GetFilePath` является одной из трех `CFileFind` функций-членов, возвращающих некоторую форму имени файла. В следующем списке описаны три и их отличия.

- Параметр [filename](#getfilename) возвращает имя файла, включая расширение. Например, вызов `GetFileName` для создания пользовательского сообщения о файле *c:\myhtml\myfile.txt* возвращает имя файла *myfile.txt*.

- `GetFilePath` Возвращает полный путь к файлу. Например, вызов `GetFilePath` для создания сообщения пользователя о файле `c:\myhtml\myfile.txt` возвращает путь к файлу `c:\myhtml\myfile.txt` .

- [Жетфилетитле](#getfiletitle) возвращает имя файла, исключая расширение файла. Например, вызов `GetFileTitle` для создания сообщения пользователя о файле *c:\myhtml\myfile.txt* Возвращает заголовок файла *MyFile*.

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: filename](#getfilename).

## <a name="cfilefindgetfiletitle"></a><a name="getfiletitle"></a> Кфилефинд:: Жетфилетитле

Вызовите эту функцию члена, чтобы получить заголовок найденного файла.

```
virtual CString GetFileTitle() const;
```

### <a name="return-value"></a>Возвращаемое значение

Заголовок файла.

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `GetFileTitle` .

`GetFileTitle` является одной из трех `CFileFind` функций-членов, возвращающих некоторую форму имени файла. В следующем списке описаны три и их отличия.

- Параметр [filename](#getfilename) возвращает имя файла, включая расширение. Например, вызов `GetFileName` для создания пользовательского сообщения о файле *c:\myhtml\myfile.txt* возвращает имя файла *myfile.txt*.

- Функция [FilePath](#getfilepath) возвращает полный путь к файлу. Например, вызов `GetFilePath` для создания сообщения пользователя о файле *c:\myhtml\myfile.txt* Возвращает путь к файлу *c:\myhtml\myfile.txt*.

- `GetFileTitle` Возвращает имя файла, исключая расширение файла. Например, вызов `GetFileTitle` для создания сообщения пользователя о файле *c:\myhtml\myfile.txt* Возвращает заголовок файла *MyFile*.

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: filename](#getfilename).

## <a name="cfilefindgetfileurl"></a><a name="getfileurl"></a> Кфилефинд:: Жетфилеурл

Вызовите эту функцию-член для получения указанного URL.

```
virtual CString GetFileURL() const;
```

### <a name="return-value"></a>Возвращаемое значение

Полный URL-адрес.

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `GetFileURL` .

`GetFileURL` функция аналогична функции-члену, за исключением [того, что](#getfilepath)она возвращает URL в форме `file://path` . Например, вызов `GetFileURL` для получения полного URL-адреса для *myfile.txt* возвращает URL-адрес `file://c:\myhtml\myfile.txt` .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: filename](#getfilename).

## <a name="cfilefindgetlastaccesstime"></a><a name="getlastaccesstime"></a> Кфилефинд:: Жетластакцесстиме

Вызовите эту функцию члена, чтобы получить время последнего доступа к заданному файлу.

```
virtual BOOL GetLastAccessTime(CTime& refTime) const;
virtual BOOL GetLastAccessTime(FILETIME* pTimeStamp) const;
```

### <a name="parameters"></a>Параметры

*рефтиме*<br/>
Ссылка на объект [CTime](../../atl-mfc-shared/reference/ctime-class.md) .

*птиместамп*<br/>
Указатель на структуру [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , содержащую время последнего обращения к файлу.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение в случае успешного выполнения; 0 в случае неудачи. `GetLastAccessTime` Возвращает 0, только если для этого объекта никогда не вызывался [FindNextFile](#findnextfile) `CFileFind` .

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `GetLastAccessTime` .

> [!NOTE]
> Не все файловые системы используют одну и ту же семантику для реализации отметки времени, возвращаемой этой функцией. Эта функция может возвращать то же значение, что и другие функции отметки времени, если базовая файловая система или сервер не поддерживает поддержание атрибута времени. Сведения о форматах времени см. в разделе Структура [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) . В некоторых операционных системах возвращенное время находится на локальном часовом поясе компьютера, где находится файл. Дополнительные сведения см. в разделе API Win32 [филетиметолокалфилетиме](/windows/win32/api/fileapi/nf-fileapi-filetimetolocalfiletime) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindgetlastwritetime"></a><a name="getlastwritetime"></a> Кфилефинд:: Жетластвритетиме

Вызовите эту функцию члена, чтобы получить время последнего изменения файла.

```
virtual BOOL GetLastWriteTime(FILETIME* pTimeStamp) const;
virtual BOOL GetLastWriteTime(CTime& refTime) const;
```

### <a name="parameters"></a>Параметры

*птиместамп*<br/>
Указатель на структуру [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , содержащую время последней запись в файл.

*рефтиме*<br/>
Ссылка на объект [CTime](../../atl-mfc-shared/reference/ctime-class.md) .

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение в случае успешного выполнения; 0 в случае неудачи. `GetLastWriteTime` Возвращает 0, только если для этого объекта никогда не вызывался [FindNextFile](#findnextfile) `CFileFind` .

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `GetLastWriteTime` .

> [!NOTE]
> Не все файловые системы используют одну и ту же семантику для реализации отметки времени, возвращаемой этой функцией. Эта функция может возвращать то же значение, что и другие функции отметки времени, если базовая файловая система или сервер не поддерживает поддержание атрибута времени. Сведения о форматах времени см. в разделе Структура [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) . В некоторых операционных системах возвращенное время находится на локальном часовом поясе компьютера, где находится файл. Дополнительные сведения см. в разделе API Win32 [филетиметолокалфилетиме](/windows/win32/api/fileapi/nf-fileapi-filetimetolocalfiletime) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindgetlength"></a><a name="getlength"></a> Кфилефинд:: DATALENGTH

Вызовите эту функцию члена, чтобы получить длину найденного файла в байтах.

```
ULONGLONG GetLength() const;
```

### <a name="return-value"></a>Возвращаемое значение

Длина найденного файла в байтах.

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `GetLength` .

`GetLength` использует структуру Win32 [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) для получения и возврата значения размера файла в байтах.

> [!NOTE]
> Начиная с MFC 7,0 `GetLength` поддерживает 64-разрядные целочисленные типы. Ранее существующий код, созданный с помощью этой более новой версии библиотеки, может привести к предупреждениям усечения.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCFiles#33](../../atl-mfc-shared/reference/codesnippet/cpp/cfilefind-class_3.cpp)]

## <a name="cfilefindgetroot"></a><a name="getroot"></a> Кфилефинд:: root

Вызовите эту функцию члена, чтобы получить корень найденного файла.

```
virtual CString GetRoot() const;
```

### <a name="return-value"></a>Возвращаемое значение

Корень активного поиска.

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `GetRoot` .

Эта функция-член возвращает описатель диска и имя пути, используемые для запуска поиска. Например, вызов [финдфиле](#findfile) с `*.dat` результатом `GetRoot` возврата пустой строки. Передача пути, например `c:\windows\system\*.dll` , в `FindFile` `GetRoot` возвращаемые результаты `c:\windows\system\` .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: filename](#getfilename).

## <a name="cfilefindisarchived"></a><a name="isarchived"></a> Кфилефинд:: Archive

Вызовите эту функцию-член, чтобы определить, архивируется ли найденный файл.

```
BOOL IsArchived() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Приложения помечают файл архива, для которого будет выполняться резервное копирование или удаление, с FILE_ATTRIBUTE_ARCHIVE атрибутом файла, определенным в структуре [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) .

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `IsArchived` .

Полный список атрибутов файла см. в функции-члене [матчесмаск](#matchesmask) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindiscompressed"></a><a name="iscompressed"></a> Кфилефинд:: уплотнение

Вызовите эту функцию-член, чтобы определить, сжат ли найденный файл.

```
BOOL IsCompressed() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Сжатый файл помечается FILE_ATTRIBUTE_COMPRESSED, атрибутом файла, определенным в структуре [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) . Для файла этот атрибут указывает, что все данные в файле сжимаются. Для каталога этот атрибут указывает на то, что для вновь создаваемых файлов и подкаталогов используется сжатие по умолчанию.

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `IsCompressed` .

Полный список атрибутов файла см. в функции-члене [матчесмаск](#matchesmask) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindisdirectory"></a><a name="isdirectory"></a> Кфилефинд:: подкаталог

Вызовите эту функцию-член, чтобы определить, является ли найденный файл каталогом.

```
BOOL IsDirectory() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Файл, являющийся каталогом, помечается FILE_ATTRIBUTE_DIRECTORY атрибутом файла, определенным в структуре [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) .

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `IsDirectory` .

Полный список атрибутов файла см. в функции-члене [матчесмаск](#matchesmask) .

### <a name="example"></a>Пример

Эта небольшая программа выполняет рекурсивный рекурсию для каждого каталога C:\. диск и выводит имя каталога.

[!code-cpp[NVC_MFCFiles#34](../../atl-mfc-shared/reference/codesnippet/cpp/cfilefind-class_4.cpp)]

## <a name="cfilefindisdots"></a><a name="isdots"></a> Кфилефинд:: наТочки

Вызывайте эту функцию-член для проверки текущего каталога и маркеров родительского каталога при переборе файлов.

```
virtual BOOL IsDots() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если найденный файл имеет имя "." или "..", что означает, что найденный файл действительно является каталогом. В противном случае 0.

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `IsDots` .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DataDirectory](#isdirectory).

## <a name="cfilefindishidden"></a><a name="ishidden"></a> Кфилефинд:: Hidden

Вызовите эту функцию-член, чтобы определить, скрыт ли найденный файл.

```
BOOL IsHidden() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Скрытые файлы, помеченные FILE_ATTRIBUTE_HIDDEN, атрибут файла, определенный в структуре [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) . Скрытый файл не включается в обычный список каталогов.

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `IsHidden` .

Полный список атрибутов файла см. в функции-члене [матчесмаск](#matchesmask) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindisnormal"></a><a name="isnormal"></a> Кфилефинд:: onобычная

Вызовите эту функцию-член, чтобы определить, является ли найденный файл обычным.

```
BOOL IsNormal() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Файлы, помеченные FILE_ATTRIBUTE_NORMAL, атрибут файла, определенный в структуре [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) . Для обычного файла не заданы другие атрибуты. Все остальные атрибуты файла переопределяют этот атрибут.

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `IsNormal` .

Полный список атрибутов файла см. в функции-члене [матчесмаск](#matchesmask) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindisreadonly"></a><a name="isreadonly"></a> Кфилефинд:: IsReadOnly

Вызовите эту функцию-член, чтобы определить, доступен ли найденный файл только для чтения.

```
BOOL IsReadOnly() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Файл, предназначенный только для чтения, помечается FILE_ATTRIBUTE_READONLY, атрибутом файла, определенным в структуре [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) . Приложения могут читать такой файл, но не могут выполнять запись в него или удалять его.

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `IsReadOnly` .

Полный список атрибутов файла см. в функции-члене [матчесмаск](#matchesmask) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindissystem"></a><a name="issystem"></a> Кфилефинд:: a System

Вызовите эту функцию-член, чтобы определить, является ли найденный файл системным.

```
BOOL IsSystem() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Системный файл помечается FILE_ATTRIBUTE_SYSTEM,, атрибутом файла, определенным в структуре [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) . Системный файл является частью или используется исключительно операционной системой.

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `IsSystem` .

Полный список атрибутов файла см. в функции-члене [матчесмаск](#matchesmask) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindistemporary"></a><a name="istemporary"></a> Кфилефинд::

Вызовите эту функцию-член, чтобы определить, является ли найденный файл временным.

```
BOOL IsTemporary() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Временный файл помечается FILE_ATTRIBUTE_TEMPORARY, атрибутом файла, определенным в структуре [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) . Временный файл используется для временного хранения. Приложения должны выполнять запись в файл только в случае крайней необходимости. Большая часть данных файла остается в памяти без записи на носитель, так как файл скоро будет удален.

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `IsTemporary` .

Полный список атрибутов файла см. в функции-члене [матчесмаск](#matchesmask) .

### <a name="example"></a>Пример

  См. пример для [кфилефинд:: DATALENGTH](#getlength).

## <a name="cfilefindm_ptm"></a><a name="m_ptm"></a> Кфилефинд:: m_pTM

Указатель на `CAtlTransactionManager` объект.

```
CAtlTransactionManager* m_pTM;
```

### <a name="remarks"></a>Комментарии

## <a name="cfilefindmatchesmask"></a><a name="matchesmask"></a> Кфилефинд:: Матчесмаск

Вызовите эту функцию-член для проверки атрибутов файла в найденном файле.

```
virtual BOOL MatchesMask(DWORD dwMask) const;
```

### <a name="parameters"></a>Параметры

*двмаск*<br/>
Задает один или несколько атрибутов файла, определенных в структуре [WIN32_FIND_DATA](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataw) , для найденного файла. Для поиска нескольких атрибутов используйте оператор побитового или (&#124;). Допустимо любое сочетание следующих атрибутов:

- FILE_ATTRIBUTE_ARCHIVE файл является архивным. Приложения используют этот атрибут для пометки файлов для резервного копирования или удаления.

- FILE_ATTRIBUTE_COMPRESSED сжатый файл или каталог. Для файла это означает, что все данные в файле сжимаются. Для каталога это означает, что для вновь создаваемых файлов и подкаталогов используется сжатие по умолчанию.

- FILE_ATTRIBUTE_DIRECTORY файл является каталогом.

- FILE_ATTRIBUTE_NORMAL для файла не заданы другие атрибуты. Этот атрибут допустим только в том случае, если он используется отдельно. Все остальные атрибуты файла переопределяют этот атрибут.

- FILE_ATTRIBUTE_HIDDEN файл скрыт. Он не должен включаться в обычный список каталогов.

- FILE_ATTRIBUTE_READONLY файл доступен только для чтения. Приложения могут считывать файл, но не могут выполнять запись в него или удалять его.

- FILE_ATTRIBUTE_SYSTEM файл является частью или используется исключительно операционной системой.

- FILE_ATTRIBUTE_TEMPORARY файл используется для временного хранения. Приложения должны выполнять запись в файл только в случае крайней необходимости. Большая часть данных файла остается в памяти без записи на носитель, так как файл скоро будет удален.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0. Чтобы получить расширенные сведения об ошибке, вызовите функцию Win32 [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

### <a name="remarks"></a>Комментарии

Необходимо вызвать [FindNextFile](#findnextfile) по крайней мере один раз перед вызовом `MatchesMask` .

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCFiles#35](../../atl-mfc-shared/reference/codesnippet/cpp/cfilefind-class_5.cpp)]

## <a name="see-also"></a>См. также раздел

[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кфтпфилефинд](../../mfc/reference/cftpfilefind-class.md)<br/>
[Класс Кгоферфилефинд](../../mfc/reference/cgopherfilefind-class.md)<br/>
[Класс Цинтернетфиле](../../mfc/reference/cinternetfile-class.md)<br/>
[Класс CGopherFile](../../mfc/reference/cgopherfile-class.md)<br/>
[Класс Чттпфиле](../../mfc/reference/chttpfile-class.md)
