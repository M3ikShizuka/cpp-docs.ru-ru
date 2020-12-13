---
description: 'Дополнительные сведения о: Крбмултимап Class'
title: Класс Крбмултимап
ms.date: 11/04/2016
f1_keywords:
- CRBMultiMap
- ATLCOLL/ATL::CRBMultiMap
- ATLCOLL/ATL::CRBMultiMap::CRBMultiMap
- ATLCOLL/ATL::CRBMultiMap::FindFirstWithKey
- ATLCOLL/ATL::CRBMultiMap::GetNextValueWithKey
- ATLCOLL/ATL::CRBMultiMap::GetNextWithKey
- ATLCOLL/ATL::CRBMultiMap::Insert
- ATLCOLL/ATL::CRBMultiMap::RemoveKey
helpviewer_keywords:
- CRBMultiMap class
ms.assetid: 94d3ec0c-3e30-4ab7-a101-d8da4fb8add3
ms.openlocfilehash: 8dfe644521cb7ec4135c5c1f71d36371ac1706ff
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141028"
---
# <a name="crbmultimap-class"></a>Класс Крбмултимап

Этот класс представляет структуру сопоставления, которая позволяет связать каждый ключ с более чем одним значением, используя Red-Black двоичное дерево.

## <a name="syntax"></a>Синтаксис

```
template<typename K,
         typename V,
         class KTraits = CElementTraits<K>,
         class VTraits = CElementTraits<V>>
class CRBMultiMap : public CRBTree<K, V, KTraits, VTraits>
```

#### <a name="parameters"></a>Параметры

*K*<br/>
Тип элемента Key.

*V*<br/>
Тип элемента value.

*ктраитс*<br/>
Код, используемый для копирования или перемещения элементов ключа. Дополнительные сведения см. в разделе [класс целементтраитс](../../atl/reference/celementtraits-class.md) .

*втраитс*<br/>
Код, используемый для копирования или перемещения элементов значений.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Крбмултимап:: Крбмултимап](#crbmultimap)|Конструктор.|
|[Крбмултимап:: ~ Крбмултимап](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Крбмултимап:: Финдфирствискэй](#findfirstwithkey)|Вызовите этот метод, чтобы найти расположение первого элемента с заданным ключом.|
|[Крбмултимап:: Жетнекствалуевискэй](#getnextvaluewithkey)|Вызовите этот метод, чтобы получить значение, связанное с заданным ключом, и обновите значение расположения.|
|[Крбмултимап:: Жетнекствискэй](#getnextwithkey)|Вызовите этот метод, чтобы получить элемент, связанный с заданным ключом, и обновите значение расположения.|
|[Крбмултимап:: INSERT](#insert)|Вызовите этот метод, чтобы вставить пару элементов в карту.|
|[Крбмултимап:: Ремовекэй](#removekey)|Вызовите этот метод, чтобы удалить все элементы ключа или значения для данного ключа.|

## <a name="remarks"></a>Комментарии

`CRBMultiMap` обеспечивает поддержку для массива сопоставления любого заданного типа, управляя упорядоченным массивом ключевых элементов и значений. В отличие от класса [крбмап](../../atl/reference/crbmap-class.md) каждый ключ может быть связан с более чем одним значением.

Элементы (состоящие из ключа и значения) хранятся в виде двоичной древовидной структуры с помощью метода [крбмултимап:: INSERT](#insert) . Элементы можно удалить с помощью метода [крбмултимап:: ремовекэй](#removekey) , который удаляет все элементы, соответствующие заданному ключу.

Обход дерева становится возможным благодаря таким методам, как [крбтри:: жесеадпоситион](../../atl/reference/crbtree-class.md#getheadposition), [Крбтри:: GetNext](../../atl/reference/crbtree-class.md#getnext)и [крбтри:: жетнекствалуе](../../atl/reference/crbtree-class.md#getnextvalue). Доступ к потенциально нескольким значениям для каждого ключа можно получить с помощью методов [крбмултимап:: финдфирствискэй](#findfirstwithkey), [Крбмултимап:: жетнекствалуевискэй](#getnextvaluewithkey)и [крбмултимап:: жетнекствискэй](#getnextwithkey) . См. пример для [крбмултимап:: крбмултимап](#crbmultimap) на практике.

Параметры *ктраитс* и *втраитс* являются признаками классов, которые содержат любой дополнительный код, необходимый для копирования или перемещения элементов.

`CRBMultiMap` является производным от [крбтри](../../atl/reference/crbtree-class.md), который реализует двоичное дерево с помощью алгоритма Red-Black. Альтернатива для `CRBMultiMap` и `CRBMap` предлагается классом [CAtlMap](../../atl/reference/catlmap-class.md) . Если необходимо сохранить небольшое количество элементов, рекомендуется использовать класс [ксимплемап](../../atl/reference/csimplemap-class.md) .

Более подробное обсуждение различных классов коллекций, их функций и характеристик производительности см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[крбтри](../../atl/reference/crbtree-class.md)

`CRBMultiMap`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="crbmultimapcrbmultimap"></a><a name="crbmultimap"></a> Крбмултимап:: Крбмултимап

Конструктор.

```
explicit CRBMultiMap(size_t nBlockSize = 10) throw();
```

### <a name="parameters"></a>Параметры

*нблокксизе*<br/>
Размер блока.

### <a name="remarks"></a>Комментарии

Параметр *нблокксизе* — это мера объема памяти, выделенной, когда требуется новый элемент. Большие размеры блоков сокращают число вызовов подпрограмм выделения памяти, но используют больше ресурсов. По умолчанию выделяется место для 10 элементов за раз.

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#85](../../atl/codesnippet/cpp/crbmultimap-class_1.cpp)]

## <a name="crbmultimapcrbmultimap"></a><a name="dtor"></a> Крбмултимап:: ~ Крбмултимап

Деструктор

```
~CRBMultiMap() throw();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы.

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

## <a name="crbmultimapfindfirstwithkey"></a><a name="findfirstwithkey"></a> Крбмултимап:: Финдфирствискэй

Вызовите этот метод, чтобы найти расположение первого элемента с заданным ключом.

```
POSITION FindFirstWithKey(KINARGTYPE key) const throw();
```

### <a name="parameters"></a>Параметры

*key*<br/>
Указывает ключ, определяющий элемент для поиска.

### <a name="return-value"></a>Возвращаемое значение

Возвращает расположение первого элемента ключа/значения, если ключ найден, в противном случае — NULL.

### <a name="remarks"></a>Комментарии

Ключ в `CRBMultiMap` может иметь одно или несколько связанных значений. Этот метод предоставит значение расположения первого значения (которое, фактически, должно быть единственным значением), связанным с этим конкретным ключом. Возвращаемое значение value может затем использоваться с [крбмултимап:: жетнекствалуевискэй](#getnextvaluewithkey) или [Крбмултимап:: жетнекствискэй](#getnextwithkey) для получения значения и обновления расположения.

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

### <a name="example"></a>Пример

См. пример для [крбмултимап:: крбмултимап](#crbmultimap).

## <a name="crbmultimapgetnextvaluewithkey"></a><a name="getnextvaluewithkey"></a> Крбмултимап:: Жетнекствалуевискэй

Вызовите этот метод, чтобы получить значение, связанное с заданным ключом, и обновите значение расположения.

```
const V& GetNextValueWithKey(
    POSITION& pos,
    KINARGTYPE key) const throw();
V& GetNextValueWithKey(
    POSITION& pos,
    KINARGTYPE key) throw();
```

### <a name="parameters"></a>Параметры

*pos*<br/>
Значение расположения, полученное с помощью вызова [крбмултимап:: финдфирствискэй](#findfirstwithkey) или [Крбмултимап:: жетнекствискэй](#getnextwithkey)или предыдущего вызова `GetNextValueWithKey` .

*key*<br/>
Указывает ключ, определяющий элемент для поиска.

### <a name="return-value"></a>Возвращаемое значение

Возвращает пару элементов, связанную с заданным ключом.

### <a name="remarks"></a>Комментарии

Значение позиции обновляется, чтобы указывать на следующее значение, связанное с ключом. Если больше нет значений, то значение параметра должно быть равно NULL.

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

### <a name="example"></a>Пример

См. пример для [крбмултимап:: крбмултимап](#crbmultimap).

## <a name="crbmultimapgetnextwithkey"></a><a name="getnextwithkey"></a> Крбмултимап:: Жетнекствискэй

Вызовите этот метод, чтобы получить элемент, связанный с заданным ключом, и обновите значение расположения.

```
const CPair* GetNextWithKey(
    POSITION& pos,
    KINARGTYPE key) const throw();
CPair* GetNextWithKey(
    POSITION& pos,
    KINARGTYPE key) throw();
```

### <a name="parameters"></a>Параметры

*pos*<br/>
Значение расположения, полученное с помощью вызова [крбмултимап:: финдфирствискэй](#findfirstwithkey) или [Крбмултимап:: жетнекствалуевискэй](#getnextvaluewithkey)или предыдущего вызова `GetNextWithKey` .

*key*<br/>
Указывает ключ, определяющий элемент для поиска.

### <a name="return-value"></a>Возвращаемое значение

Возвращает следующий элемент [класса крбтри:: кпаир](crbtree-class.md#cpair_class) , связанный с заданным ключом.

### <a name="remarks"></a>Комментарии

Значение позиции обновляется, чтобы указывать на следующее значение, связанное с ключом. Если больше нет значений, то значение параметра должно быть равно NULL.

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

## <a name="crbmultimapinsert"></a><a name="insert"></a> Крбмултимап:: INSERT

Вызовите этот метод, чтобы вставить пару элементов в карту.

```
POSITION Insert(KINARGTYPE key, VINARGTYPE value) throw(...);
```

### <a name="parameters"></a>Параметры

*key*<br/>
Значение ключа, добавляемое в `CRBMultiMap` объект.

*value*<br/>
Значение, добавляемое в `CRBMultiMap` объект, связанное с *ключом*.

### <a name="return-value"></a>Возвращаемое значение

Возвращает расположение пары элементов "ключ-значение" в `CRBMultiMap` объекте.

### <a name="remarks"></a>Комментарии

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

### <a name="example"></a>Пример

См. пример для [крбмултимап:: крбмултимап](#crbmultimap).

## <a name="crbmultimapremovekey"></a><a name="removekey"></a> Крбмултимап:: Ремовекэй

Вызовите этот метод, чтобы удалить все элементы ключа или значения для данного ключа.

```
size_t RemoveKey(KINARGTYPE key) throw();
```

### <a name="parameters"></a>Параметры

*key*<br/>
Указывает ключ, определяющий удаляемые элементы.

### <a name="return-value"></a>Возвращаемое значение

Возвращает число значений, связанных с заданным ключом.

### <a name="remarks"></a>Комментарии

`RemoveKey` Удаляет все элементы ключа или значения, имеющие ключ, совпадающий с *ключом*.

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

### <a name="example"></a>Пример

См. пример для [крбмултимап:: крбмултимап](#crbmultimap).

## <a name="see-also"></a>См. также раздел

[Класс Крбтри](../../atl/reference/crbtree-class.md)<br/>
[Класс CAtlMap](../../atl/reference/catlmap-class.md)<br/>
[Класс Крбмап](../../atl/reference/crbmap-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
