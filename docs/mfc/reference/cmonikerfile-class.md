---
description: 'Дополнительные сведения о: Кмоникерфиле Class'
title: Класс Кмоникерфиле
ms.date: 11/04/2016
f1_keywords:
- CMonikerFile
- AFXOLE/CMonikerFile
- AFXOLE/CMonikerFile::CMonikerFile
- AFXOLE/CMonikerFile::Close
- AFXOLE/CMonikerFile::Detach
- AFXOLE/CMonikerFile::GetMoniker
- AFXOLE/CMonikerFile::Open
- AFXOLE/CMonikerFile::CreateBindContext
helpviewer_keywords:
- CMonikerFile [MFC], CMonikerFile
- CMonikerFile [MFC], Close
- CMonikerFile [MFC], Detach
- CMonikerFile [MFC], GetMoniker
- CMonikerFile [MFC], Open
- CMonikerFile [MFC], CreateBindContext
ms.assetid: 87be5966-f4f7-4235-bce2-1fa39e9417de
ms.openlocfilehash: d59de05f688c10d3dbfa6682777d5fd11d4f53ec
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331587"
---
# <a name="cmonikerfile-class"></a>Класс Кмоникерфиле

Представляет поток данных ( [IStream](/windows/win32/api/objidl/nn-objidl-istream)) с именем [IMoniker](/windows/win32/api/objidl/nn-objidl-imoniker).

## <a name="syntax"></a>Синтаксис

```
class CMonikerFile : public COleStreamFile
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмоникерфиле:: Кмоникерфиле](#cmonikerfile)|Формирует объект `CMonikerFile`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмоникерфиле:: Close](#close)|Отсоединяет и освобождает поток и освобождает моникер.|
|[Кмоникерфиле::D етач](#detach)|Отсоединяет `IMoniker` объект от этого `CMonikerFile` объекта.|
|[Кмоникерфиле:: моникер](#getmoniker)|Возвращает текущий моникер.|
|[Кмоникерфиле:: Open](#open)|Открывает указанный файл для получения потока.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кмоникерфиле:: Креатебиндконтекст](#createbindcontext)|Получает контекст привязки или создает инициализированный контекст привязки по умолчанию.|

## <a name="remarks"></a>Комментарии

Моникер содержит информацию, похожую на путь к файлу. Если у вас есть указатель на интерфейс объекта моникера `IMoniker` , можно получить доступ к определенному файлу, не имея никаких других сведений о том, где фактически находится файл.

Производный от `COleStreamFile` , `CMonikerFile` принимает моникер или строковое представление, которое можно преобразовать в моникер и привязывает к потоку, для которого имя моникера является именем. Затем можно выполнять чтение и запись в этот поток. Реальная цель `CMonikerFile` заключается в том, чтобы предоставить простой доступ к с `IStream` именем с помощью `IMoniker` s, чтобы не привязываться к потоку самостоятельно, но в `CFile` нем есть функции для потока.

`CMonikerFile` не может использоваться для привязки к чему-либо, кроме потока. Если требуется выполнить привязку к хранилищу или объекту, необходимо `IMoniker` напрямую использовать интерфейс.

Дополнительные сведения о потоках и моникерах см. в разделе [колестреамфиле](../../mfc/reference/colestreamfile-class.md) в *справочнике по MFC* и [IStream](/windows/win32/api/objidl/nn-objidl-istream) и [IMoniker](/windows/win32/api/objidl/nn-objidl-imoniker) в Windows SDK.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CFile](../../mfc/reference/cfile-class.md)

[COleStreamFile](../../mfc/reference/colestreamfile-class.md)

`CMonikerFile`

## <a name="requirements"></a>Требования

**Заголовок:** афксоле. h

## <a name="cmonikerfileclose"></a><a name="close"></a> Кмоникерфиле:: Close

Вызовите эту функцию, чтобы отсоединить и освободить поток и освободить моникер.

```
virtual void Close();
```

### <a name="remarks"></a>Комментарии

Может вызываться для неоткрытых или уже закрытых потоков.

## <a name="cmonikerfilecmonikerfile"></a><a name="cmonikerfile"></a> Кмоникерфиле:: Кмоникерфиле

Формирует объект `CMonikerFile`.

```
CMonikerFile();
```

## <a name="cmonikerfilecreatebindcontext"></a><a name="createbindcontext"></a> Кмоникерфиле:: Креатебиндконтекст

Вызовите эту функцию, чтобы создать инициализированный по умолчанию контекст привязки.

```
IBindCtx* CreateBindContext(CFileException* pError);
```

### <a name="parameters"></a>Параметры

*pError*<br/>
Указатель на исключение файла. В случае ошибки будет задана причина.

### <a name="return-value"></a>Возвращаемое значение

Указатель на контекст привязки [IBindCtx](/windows/win32/api/objidl/nn-objidl-ibindctx) для привязки в случае успеха; в противном случае — NULL. Если экземпляр был открыт с помощью `IBindHost` интерфейса, контекст привязки извлекается из `IBindHost` . Если `IBindHost` интерфейс отсутствует или интерфейс не может вернуть контекст привязки, создается контекст привязки. Описание интерфейса [ибиндхост](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076\(v=vs.85\)) см. Windows SDK.

### <a name="remarks"></a>Комментарии

Контекст привязки — это объект, хранящий сведения о конкретной операции привязки моникера. Эту функцию можно переопределить для предоставления пользовательского контекста привязки.

## <a name="cmonikerfiledetach"></a><a name="detach"></a> Кмоникерфиле::D етач

Вызовите эту функцию, чтобы закрыть поток.

```
BOOL Detach(CFileException* pError = NULL);
```

### <a name="parameters"></a>Параметры

*pError*<br/>
Указатель на исключение файла. В случае ошибки будет задана причина.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

## <a name="cmonikerfilegetmoniker"></a><a name="getmoniker"></a> Кмоникерфиле:: моникер

Вызовите эту функцию, чтобы получить указатель на текущий моникер.

```
IMoniker* GetMoniker() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на текущий интерфейс моникера ( [IMoniker](/windows/win32/api/objidl/nn-objidl-imoniker)).

### <a name="remarks"></a>Комментарии

Поскольку не `CMonikerFile` является интерфейсом, возвращаемый указатель не увеличивает число ссылок (через [AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)), а моникер освобождается при `CMonikerFile` освобождении объекта. Если вы хотите хранить моникер или освободить его самостоятельно, вам необходимо `AddRef` .

## <a name="cmonikerfileopen"></a><a name="open"></a> Кмоникерфиле:: Open

Вызовите эту функцию-член, чтобы открыть файл или объект моникера.

```
virtual BOOL Open(
    LPCTSTR lpszURL,
    CFileException* pError = NULL);

virtual BOOL Open(
    IMoniker* pMoniker,
    CFileException* pError = NULL);
```

### <a name="parameters"></a>Параметры

*лпсзурл*<br/>
URL-адрес или имя файла, который будет открыт.

*pError*<br/>
Указатель на исключение файла. В случае ошибки будет задана причина.

*пмоникер*<br/>
Указатель на интерфейс моникера, `IMoniker` используемый для получения потока.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Параметр *лпсзурл* нельзя использовать для Macintosh.  `Open` Для Macintosh можно использовать только форму пмоникер.

Для параметра *лпсзурл* можно использовать URL-адрес или имя файла. Пример:

[!code-cpp[NVC_MFCWinInet#6](../../mfc/codesnippet/cpp/cmonikerfile-class_1.cpp)]

\- или -

[!code-cpp[NVC_MFCWinInet#7](../../mfc/codesnippet/cpp/cmonikerfile-class_2.cpp)]

## <a name="see-also"></a>См. также раздел

[Класс Колестреамфиле](../../mfc/reference/colestreamfile-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Касинкмоникерфиле](../../mfc/reference/casyncmonikerfile-class.md)
