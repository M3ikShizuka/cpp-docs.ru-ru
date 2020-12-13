---
description: 'Дополнительные сведения о: Иперсистсторажеимпл Class'
title: Класс Иперсистсторажеимпл
ms.date: 11/04/2016
f1_keywords:
- IPersistStorageImpl
- ATLCOM/ATL::IPersistStorageImpl
- ATLCOM/ATL::IPersistStorageImpl::GetClassID
- ATLCOM/ATL::IPersistStorageImpl::HandsOffStorage
- ATLCOM/ATL::IPersistStorageImpl::InitNew
- ATLCOM/ATL::IPersistStorageImpl::IsDirty
- ATLCOM/ATL::IPersistStorageImpl::Load
- ATLCOM/ATL::IPersistStorageImpl::Save
- ATLCOM/ATL::IPersistStorageImpl::SaveCompleted
helpviewer_keywords:
- storage, ATL
- IPersistStorageImpl class
ms.assetid: d652f02c-239c-47c7-9a50-3e9fc3014fff
ms.openlocfilehash: 1d3d996886b587c25988139eed62e409650b5d4e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139338"
---
# <a name="ipersiststorageimpl-class"></a>Класс Иперсистсторажеимпл

Этот класс реализует интерфейс [иперсистстораже](/windows/win32/api/objidl/nn-objidl-ipersiststorage) .

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <class T>
class ATL_NO_VTABLE IPersistStorageImpl : public IPersistStorage
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IPersistStorageImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иперсистсторажеимпл::, ClassID](#getclassid)|Получает CLSID объекта.|
|[Иперсистсторажеимпл:: Хандсоффстораже](#handsoffstorage)|Указывает объекту освободить все объекты хранилища и войти в режим Хандсофф. Реализация ATL возвращает S_OK.|
|[Иперсистсторажеимпл:: InitNew](#initnew)|Инициализирует новое хранилище.|
|[Иперсистсторажеимпл:: IsDirty](#isdirty)|Проверяет, изменились ли данные объекта со времени последнего сохранения.|
|[Иперсистсторажеимпл:: Load](#load)|Загружает свойства объекта из указанного хранилища.|
|[Иперсистсторажеимпл:: Save](#save)|Сохраняет свойства объекта в указанном хранилище.|
|[Иперсистсторажеимпл:: Савекомплетед](#savecompleted)|Сообщает объекту, что он может вернуться в нормальный режим для записи в свой объект хранилища. Реализация ATL возвращает S_OK.|

## <a name="remarks"></a>Комментарии

`IPersistStorageImpl` реализует интерфейс [иперсистстораже](/windows/win32/api/objidl/nn-objidl-ipersiststorage) , позволяющий клиенту запрашивать загрузку объекта и сохранять постоянные данные с помощью хранилища.

Реализация этого класса требует класс `T` , чтобы реализовать `IPersistStreamInit` интерфейс, доступный через `QueryInterface` . Обычно это означает, что класс `T` должен быть производным от [IPersistStreamInitImpl](../../atl/reference/ipersiststreaminitimpl-class.md), предоставлять запись для `IPersistStreamInit` в [сопоставлении com](com-map-macros.md)и использовать [карту свойств](property-map-macros.md) для описания постоянных данных класса.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IPersistStorage`

`IPersistStorageImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ipersiststorageimplgetclassid"></a><a name="getclassid"></a> Иперсистсторажеимпл::, ClassID

Получает CLSID объекта.

```
STDMETHOD(GetClassID)(CLSID* pClassID);
```

### <a name="remarks"></a>Комментарии

См. [IPersist:: ClassID](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) в Windows SDK.

## <a name="ipersiststorageimplhandsoffstorage"></a><a name="handsoffstorage"></a> Иперсистсторажеимпл:: Хандсоффстораже

Указывает объекту освободить все объекты хранилища и войти в режим Хандсофф.

```
STDMETHOD(HandsOffStorage)(void);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [иперсистстораже:: хандсоффстораже](/windows/win32/api/objidl/nf-objidl-ipersiststorage-handsoffstorage) в Windows SDK.

## <a name="ipersiststorageimplinitnew"></a><a name="initnew"></a> Иперсистсторажеимпл:: InitNew

Инициализирует новое хранилище.

```
STDMETHOD(InitNew)(IStorage*);
```

### <a name="remarks"></a>Комментарии

Реализация ATL делегирует интерфейсу [иперсистстреаминит](/windows/win32/api/ocidl/nn-ocidl-ipersiststreaminit) .

См. раздел [иперсистстораже: InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) в Windows SDK.

## <a name="ipersiststorageimplisdirty"></a><a name="isdirty"></a> Иперсистсторажеимпл:: IsDirty

Проверяет, изменились ли данные объекта со времени последнего сохранения.

```
STDMETHOD(IsDirty)(void);
```

### <a name="remarks"></a>Комментарии

Реализация ATL делегирует интерфейсу [иперсистстреаминит](/windows/win32/api/ocidl/nn-ocidl-ipersiststreaminit) .

См. раздел [иперсистстораже: IsDirty](/windows/win32/api/objidl/nf-objidl-ipersiststorage-isdirty) в Windows SDK.

## <a name="ipersiststorageimplload"></a><a name="load"></a> Иперсистсторажеимпл:: Load

Загружает свойства объекта из указанного хранилища.

```
STDMETHOD(Load)(IStorage* pStorage);
```

### <a name="remarks"></a>Комментарии

Реализация ATL делегирует интерфейсу [иперсистстреаминит](/windows/win32/api/ocidl/nn-ocidl-ipersiststreaminit) . `Load` использует поток с именем "Content" для получения данных объекта. Метод [Save](#save) изначально создает этот поток.

См. раздел [иперсистстораже: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) в Windows SDK.

## <a name="ipersiststorageimplsave"></a><a name="save"></a> Иперсистсторажеимпл:: Save

Сохраняет свойства объекта в указанном хранилище.

```
STDMETHOD(Save)(IStorage* pStorage, BOOL fSameAsLoad);
```

### <a name="remarks"></a>Комментарии

Реализация ATL делегирует интерфейсу [иперсистстреаминит](/windows/win32/api/ocidl/nn-ocidl-ipersiststreaminit) . При `Save` первом вызове создается поток с именем "Content" (содержимое) в указанном хранилище. Этот поток затем используется в последующих вызовах функций `Save` и в вызовах для [загрузки](#load).

См. раздел [иперсистстораже: Save](/windows/win32/api/objidl/nf-objidl-ipersiststorage-save) в Windows SDK.

## <a name="ipersiststorageimplsavecompleted"></a><a name="savecompleted"></a> Иперсистсторажеимпл:: Савекомплетед

Сообщает объекту, что он может вернуться в нормальный режим для записи в свой объект хранилища.

```
STDMETHOD(SaveCompleted)(IStorage*);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [иперсистстораже: савекомплетед](/windows/win32/api/objidl/nf-objidl-ipersiststorage-savecompleted) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Хранилища и потоки](/windows/win32/Stg/storages-and-streams)<br/>
[Класс IPersistStreamInitImpl](../../atl/reference/ipersiststreaminitimpl-class.md)<br/>
[Класс Иперсистпропертибагимпл](../../atl/reference/ipersistpropertybagimpl-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
