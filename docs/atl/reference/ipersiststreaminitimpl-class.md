---
description: 'Дополнительные сведения о: IPersistStreamInitImpl Class'
title: Класс IPersistStreamInitImpl
ms.date: 11/04/2016
f1_keywords:
- IPersistStreamInitImpl
- ATLCOM/ATL::IPersistStreamInitImpl
- ATLCOM/ATL::IPersistStreamInitImpl::GetClassID
- ATLCOM/ATL::IPersistStreamInitImpl::GetSizeMax
- ATLCOM/ATL::IPersistStreamInitImpl::InitNew
- ATLCOM/ATL::IPersistStreamInitImpl::IsDirty
- ATLCOM/ATL::IPersistStreamInitImpl::Load
- ATLCOM/ATL::IPersistStreamInitImpl::Save
helpviewer_keywords:
- IPersistStreamInit ATL implementation
- IPersistStreamInitImpl class
- streams, ATL
ms.assetid: ef217c3c-020f-4cf8-871e-ef68e57865b8
ms.openlocfilehash: f60483435be750c7031f2e7bf7f3f18cba36a023
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158157"
---
# <a name="ipersiststreaminitimpl-class"></a>Класс IPersistStreamInitImpl

Этот класс реализует `IUnknown` интерфейс [иперсистстреаминит](/windows/win32/api/ocidl/nn-ocidl-ipersiststreaminit) и предоставляет реализацию по умолчанию.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T>
class ATL_NO_VTABLE IPersistStreamInitImpl
   : public IPersistStreamInit
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IPersistStreamInitImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[IPersistStreamInitImpl::, ClassID](#getclassid)|Получает CLSID объекта.|
|[IPersistStreamInitImpl:: Жетсиземакс](#getsizemax)|Возвращает размер потока, необходимого для сохранения данных объекта. Реализация ATL возвращает E_NOTIMPL.|
|[IPersistStreamInitImpl:: InitNew](#initnew)|Инициализирует вновь созданный объект.|
|[IPersistStreamInitImpl:: IsDirty](#isdirty)|Проверяет, изменились ли данные объекта со времени последнего сохранения.|
|[IPersistStreamInitImpl:: Load](#load)|Загружает свойства объекта из указанного потока.|
|[IPersistStreamInitImpl:: Save](#save)|Сохраняет свойства объекта в указанный поток.|

## <a name="remarks"></a>Комментарии

Интерфейс [иперсистстреаминит](/windows/win32/api/ocidl/nn-ocidl-ipersiststreaminit) позволяет клиенту запрашивать загрузку объекта и сохранять его постоянные данные в один поток. Класс `IPersistStreamInitImpl` предоставляет реализацию этого интерфейса по умолчанию и реализует `IUnknown` , отправляя сведения в устройство дампа в отладочных сборках.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IPersistStreamInit`

`IPersistStreamInitImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ipersiststreaminitimplgetclassid"></a><a name="getclassid"></a> IPersistStreamInitImpl::, ClassID

Получает CLSID объекта.

```
STDMETHOD(GetClassID)(CLSID* pClassID);
```

### <a name="remarks"></a>Комментарии

См. [IPersist:: ClassID](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) в Windows SDK.

## <a name="ipersiststreaminitimplgetsizemax"></a><a name="getsizemax"></a> IPersistStreamInitImpl:: Жетсиземакс

Возвращает размер потока, необходимого для сохранения данных объекта.

```
STDMETHOD(GetSizeMax)(ULARGE_INTEGER FAR* pcbSize);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает E_NOTIMPL.

### <a name="remarks"></a>Комментарии

См. раздел [иперсистстреаминит:: жетсиземакс](/windows/win32/api/ocidl/nf-ocidl-ipersiststreaminit-getsizemax) в Windows SDK.

## <a name="ipersiststreaminitimplinitnew"></a><a name="initnew"></a> IPersistStreamInitImpl:: InitNew

Инициализирует вновь созданный объект.

```
STDMETHOD(InitNew)();
```

### <a name="remarks"></a>Комментарии

См. раздел [иперсистстреаминит:: InitNew](/windows/win32/api/ocidl/nf-ocidl-ipersiststreaminit-initnew) в Windows SDK.

## <a name="ipersiststreaminitimplisdirty"></a><a name="isdirty"></a> IPersistStreamInitImpl:: IsDirty

Проверяет, изменились ли данные объекта со времени последнего сохранения.

```
STDMETHOD(IsDirty)();
```

### <a name="remarks"></a>Комментарии

См. раздел [иперсистстреаминит:: IsDirty](/windows/win32/api/ocidl/nf-ocidl-ipersiststreaminit-isdirty) в Windows SDK.

## <a name="ipersiststreaminitimplload"></a><a name="load"></a> IPersistStreamInitImpl:: Load

Загружает свойства объекта из указанного потока.

```
STDMETHOD(Load)(LPSTREAM pStm);
```

### <a name="remarks"></a>Комментарии

Для получения этих сведений в ATL используется схема свойств объекта.

См. раздел [иперсистстреаминит:: Load](/windows/win32/api/ocidl/nf-ocidl-ipersiststreaminit-load) в Windows SDK.

## <a name="ipersiststreaminitimplsave"></a><a name="save"></a> IPersistStreamInitImpl:: Save

Сохраняет свойства объекта в указанный поток.

```
STDMETHOD(Save)(LPSTREAM pStm, BOOL fClearDirty);
```

### <a name="remarks"></a>Комментарии

Для хранения этих сведений в ATL используется схема свойств объекта.

См. раздел [иперсистстреаминит:: Save](/windows/win32/api/ocidl/nf-ocidl-ipersiststreaminit-save) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Хранилища и потоки](/windows/win32/Stg/storages-and-streams)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
