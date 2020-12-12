---
description: 'Дополнительные сведения о: Колестреамфиле Class'
title: Класс Колестреамфиле
ms.date: 11/04/2016
f1_keywords:
- COleStreamFile
- AFXOLE/COleStreamFile
- AFXOLE/COleStreamFile::COleStreamFile
- AFXOLE/COleStreamFile::Attach
- AFXOLE/COleStreamFile::CreateMemoryStream
- AFXOLE/COleStreamFile::CreateStream
- AFXOLE/COleStreamFile::Detach
- AFXOLE/COleStreamFile::GetStream
- AFXOLE/COleStreamFile::OpenStream
helpviewer_keywords:
- COleStreamFile [MFC], COleStreamFile
- COleStreamFile [MFC], Attach
- COleStreamFile [MFC], CreateMemoryStream
- COleStreamFile [MFC], CreateStream
- COleStreamFile [MFC], Detach
- COleStreamFile [MFC], GetStream
- COleStreamFile [MFC], OpenStream
ms.assetid: e4f93698-e17c-4a18-a7c0-4b4df8eb4d93
ms.openlocfilehash: b856dc5b408c43f61a11f7c68035587bc16bbeaa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226640"
---
# <a name="colestreamfile-class"></a>Класс Колестреамфиле

Представляет поток данных (`IStream`) в составном файле как часть структурированного хранения OLE.

## <a name="syntax"></a>Синтаксис

```
class COleStreamFile : public CFile
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Колестреамфиле:: Колестреамфиле](#colestreamfile)|Формирует объект `COleStreamFile`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Колестреамфиле:: Attach](#attach)|Связывает поток с объектом.|
|[Колестреамфиле:: Креатемемористреам](#creatememorystream)|Создает поток из глобальной памяти и связывает его с объектом.|
|[Колестреамфиле:: Креатестреам](#createstream)|Создает поток и связывает его с объектом.|
|[Колестреамфиле::D етач](#detach)|Отменяет связь потока от объекта.|
|[Колестреамфиле:: Stream](#getstream)|Возвращает текущий поток.|
|[Колестреамфиле:: Опенстреам](#openstream)|Безопасно открывает поток и связывает его с объектом.|

## <a name="remarks"></a>Комментарии

`IStorage`Объект должен существовать, прежде чем можно будет открыть или создать поток, если он не является потоком памяти.

`COleStreamFile` объекты обрабатываются точно так же, как объекты [кфиле](../../mfc/reference/cfile-class.md) .

Дополнительные сведения об управлении потоками и хранилищами см. в разделе [контейнеры статей: составные файлы](../../mfc/containers-compound-files.md).

Дополнительные сведения см. в разделе [IStream](/windows/win32/api/objidl/nn-objidl-istream) и [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) в Windows SDK.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CFile](../../mfc/reference/cfile-class.md)

`COleStreamFile`

## <a name="requirements"></a>Требования

**Заголовок:** афксоле. h

## <a name="colestreamfileattach"></a><a name="attach"></a> Колестреамфиле:: Attach

Связывает переданный поток OLE с `COleStreamFile` объектом.

```cpp
void Attach(LPSTREAM lpStream);
```

### <a name="parameters"></a>Параметры

*лпстреам*<br/>
Указывает на поток OLE ( `IStream` ), который должен быть связан с объектом. Не может быть NULL.

### <a name="remarks"></a>Комментарии

Объект не должен быть уже связан с потоком OLE.

Дополнительные сведения см. в разделе [IStream](/windows/win32/api/objidl/nn-objidl-istream) в Windows SDK.

## <a name="colestreamfilecolestreamfile"></a><a name="colestreamfile"></a> Колестреамфиле:: Колестреамфиле

Создает объект `COleStreamFile`.

```
COleStreamFile(LPSTREAM lpStream = NULL);
```

### <a name="parameters"></a>Параметры

*лпстреам*<br/>
Указатель на поток OLE, который должен быть связан с объектом.

### <a name="remarks"></a>Комментарии

Если *лпстреам* имеет значение null, объект не связан с потоком OLE, в противном случае объект связывается с предоставляемым потоком OLE.

Дополнительные сведения см. в разделе [IStream](/windows/win32/api/objidl/nn-objidl-istream) в Windows SDK.

## <a name="colestreamfilecreatememorystream"></a><a name="creatememorystream"></a> Колестреамфиле:: Креатемемористреам

Безопасно создает новый поток из глобальной общей памяти, в которой сбой является нормальным, ожидаемым условием.

```
BOOL CreateMemoryStream(CFileException* pError = NULL);
```

### <a name="parameters"></a>Параметры

*pError*<br/>
Указывает на объект [кфиликсцептион](../../mfc/reference/cfileexception-class.md) или значение null, указывающее состояние завершения операции создания. Укажите этот параметр, если требуется отслеживать возможные исключения, созданные при попытке создать поток.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если поток успешно создан; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Память выделяется подсистемой OLE.

Дополнительные сведения см. в разделе [CreateStreamOnHGlobal](/windows/win32/api/combaseapi/nf-combaseapi-createstreamonhglobal) в Windows SDK.

## <a name="colestreamfilecreatestream"></a><a name="createstream"></a> Колестреамфиле:: Креатестреам

Безопасно создает новый поток в указанном объекте хранилища, в котором сбой является нормальным ожидаемым условием.

```
BOOL CreateStream(
    LPSTORAGE lpStorage,
    LPCTSTR lpszStreamName,
    DWORD nOpenFlags = modeReadWrite|shareExclusive|modeCreate,
    CFileException* pError = NULL);
```

### <a name="parameters"></a>Параметры

*лпстораже*<br/>
Указывает на объект OLE Storage, содержащий создаваемый поток. Не может быть NULL.

*лпсзстреамнаме*<br/>
Имя создаваемого потока. Не может быть NULL.

*нопенфлагс*<br/>
Режим доступа для использования при открытии потока. По умолчанию используются монопольные режимы, доступные для чтения, записи и создания. Полный список доступных режимов см. в разделе [кфиле:: кфиле](../../mfc/reference/cfile-class.md#cfile).

*pError*<br/>
Указывает на объект [кфиликсцептион](../../mfc/reference/cfileexception-class.md) или значение null. Укажите этот параметр, если требуется отслеживать возможные исключения, созданные при попытке создать поток.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если поток успешно создан; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Исключение файла будет выдано, если открытые ошибки и *perror* не равны NULL.

Дополнительные сведения см. в разделе [IStorage:: креатестреам](/windows/win32/api/objidl/nf-objidl-istorage-createstream) в Windows SDK.

## <a name="colestreamfiledetach"></a><a name="detach"></a> Колестреамфиле::D етач

Отменяет связь потока от объекта, не закрывая поток.

```
LPSTREAM Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на поток ( `IStream` ), связанный с объектом.

### <a name="remarks"></a>Комментарии

Перед завершением программы поток должен быть закрыт другим способом.

Дополнительные сведения см. в разделе [IStream](/windows/win32/api/objidl/nn-objidl-istream) в Windows SDK.

## <a name="colestreamfilegetstream"></a><a name="getstream"></a> Колестреамфиле:: Stream

Вызовите эту функцию, чтобы вернуть указатель на текущий поток.

```
IStream* GetStream() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на текущий интерфейс потока ( [IStream](/windows/win32/api/objidl/nn-objidl-istream)).

## <a name="colestreamfileopenstream"></a><a name="openstream"></a> Колестреамфиле:: Опенстреам

Открывает существующий поток.

```
BOOL OpenStream(
    LPSTORAGE lpStorage,
    LPCTSTR lpszStreamName,
    DWORD nOpenFlags = modeReadWrite|shareExclusive,
    CFileException* pError = NULL);
```

### <a name="parameters"></a>Параметры

*лпстораже*<br/>
Указывает на объект OLE Storage, который содержит открываемый поток. Не может быть NULL.

*лпсзстреамнаме*<br/>
Имя открываемого потока. Не может быть NULL.

*нопенфлагс*<br/>
Режим доступа для использования при открытии потока. Монопольный режим и режимы чтения и записи используются по умолчанию. Полный список доступных режимов см. в разделе [кфиле:: кфиле](../../mfc/reference/cfile-class.md#cfile).

*pError*<br/>
Указывает на объект [кфиликсцептион](../../mfc/reference/cfileexception-class.md) или значение null. Укажите этот параметр, если требуется отслеживать возможные исключения, созданные при попытке открыть поток.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если поток открыт успешно. в противном случае — 0.

### <a name="remarks"></a>Комментарии

Исключение файла будет выдано, если открытые ошибки и *perror* не равны NULL.

Дополнительные сведения см. в разделе [IStorage:: опенстреам](/windows/win32/api/objidl/nf-objidl-istorage-openstream) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Класс Кфиле](../../mfc/reference/cfile-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
