---
description: 'Дополнительные сведения о: Иколлектиононстлимпл Class'
title: Класс Иколлектиононстлимпл
ms.date: 11/04/2016
f1_keywords:
- ICollectionOnSTLImpl
- ATLCOM/ATL::ICollectionOnSTLImpl
- ATLCOM/ATL::ICollectionOnSTLImpl::get__NewEnum
- ATLCOM/ATL::ICollectionOnSTLImpl::getcount
- ATLCOM/ATL::ICollectionOnSTLImpl::get_Item
- ATLCOM/ATL::ICollectionOnSTLImpl::m_coll
helpviewer_keywords:
- ICollectionOnSTLImpl class
ms.assetid: 683c88b0-0d97-4779-a762-e493334ba7f9
ms.openlocfilehash: 089fc0fbd8f410d740646e2a653b076d32448647
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139611"
---
# <a name="icollectiononstlimpl-class"></a>Класс Иколлектиононстлимпл

Этот класс предоставляет методы, используемые классом коллекции.

## <a name="syntax"></a>Синтаксис

```
template <class T, class CollType, class ItemType, class CopyItem, class EnumType>
class ICollectionOnSTLImpl : public T
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Интерфейс коллекции COM.

*коллтипе*<br/>
Класс контейнера стандартной библиотеки C++.

*ItemType*<br/>
Тип элемента, предоставляемого интерфейсом контейнера.

*CopyItem*<br/>
[Класс политики копирования](../../atl/atl-copy-policy-classes.md).

*EnumType*<br/>
Класс перечислителя, совместимый с [ккоменумонстл](../../atl/reference/ccomenumonstl-class.md).

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иколлектиононстлимпл:: get__NewEnum](#newenum)|Возвращает объект перечислителя для коллекции.|
|[Иколлектиононстлимпл:: NOCOUNT](#get_count)|Возвращает количество элементов в коллекции.|
|[Иколлектиононстлимпл:: get_Item](#get_item)|Возвращает запрошенный элемент из коллекции.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Иколлектиононстлимпл:: m_coll](#m_coll)|Коллекция.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет реализацию для трех методов интерфейса коллекции: [NOCOUNT](#get_count), [get_Item](#get_item)и [get__NewEnum](#newenum).

Чтобы использовать этот класс, сделайте следующее:

- Определите (или создайте) интерфейс коллекции, который вы хотите реализовать.

- Создайте класс, производный от специализации, `ICollectionOnSTLImpl` на основе этого интерфейса коллекции.

- Используйте производный класс для реализации любых методов из интерфейса коллекции, который не обрабатывается `ICollectionOnSTLImpl` .

> [!NOTE]
> Если интерфейс коллекции является сдвоенным интерфейсом, создайте класс, производный от [IDispatchImpl](../../atl/reference/idispatchimpl-class.md), передав `ICollectionOnSTLImpl` специализацию в качестве первого параметра шаблона, если вы хотите, чтобы ATL предоставил реализацию `IDispatch` методов.

- Добавьте элементы в элемент [m_coll](#m_coll) , чтобы заполнить коллекцию.

Дополнительные сведения и примеры см. в разделе [коллекции и перечислители ATL](../../atl/atl-collections-and-enumerators.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`T`

`ICollectionOnSTLImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="icollectiononstlimplgetcount"></a><a name="get_count"></a> Иколлектиононстлимпл:: NOCOUNT

Этот метод возвращает количество элементов в коллекции.

```
STDMETHOD(getcount)(long* pcount);
```

### <a name="parameters"></a>Параметры

*pcount*<br/>
заполняет Число элементов в коллекции.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

## <a name="icollectiononstlimplget_item"></a><a name="get_item"></a> Иколлектиононстлимпл:: get_Item

Этот метод возвращает указанный элемент из коллекции.

```
STDMETHOD(get_Item)(long Index, ItemType* pvar);
```

### <a name="parameters"></a>Параметры

*Index*<br/>
окне Отсчитываемый от 1 индекс элемента в коллекции.

*пвар*<br/>
заполняет Элемент, соответствующий *индексу*.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

Элемент получается путем копирования данных в указанной позиции в [m_coll](#m_coll) с помощью метода Copy [класса политики копирования](../../atl/atl-copy-policy-classes.md) , переданного в качестве аргумента шаблона в `ICollectionOnSTLImpl` специализации.

## <a name="icollectiononstlimplget__newenum"></a><a name="newenum"></a> Иколлектиононстлимпл:: get__NewEnum

Возвращает объект перечислителя для коллекции.

```
STDMETHOD(get__NewEnum)(IUnknown** ppUnk);
```

### <a name="parameters"></a>Параметры

*ппунк*<br/>
заполняет Указатель **IUnknown** созданного объекта перечислителя.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

Созданный перечислитель поддерживает итератор исходной коллекции, `m_coll` (поэтому копирование не выполняется) и содержит ссылку COM на объект коллекции, чтобы гарантировать, что коллекция остается в активном состоянии при наличии необработанных перечислителей.

## <a name="icollectiononstlimplm_coll"></a><a name="m_coll"></a> Иколлектиононстлимпл:: m_coll

Этот элемент содержит элементы, представленные коллекцией.

```
CollType m_coll;
```

## <a name="see-also"></a>См. также раздел

[Пример Атлколлектионс](../../overview/visual-cpp-samples.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
