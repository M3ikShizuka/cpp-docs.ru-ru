---
description: 'Дополнительные сведения о: Крбмап Class'
title: Класс Крбмап
ms.date: 11/04/2016
f1_keywords:
- CRBMap
- ATLCOLL/ATL::CRBMap
- ATLCOLL/ATL::CRBMap::CRBMap
- ATLCOLL/ATL::CRBMap::Lookup
- ATLCOLL/ATL::CRBMap::RemoveKey
- ATLCOLL/ATL::CRBMap::SetAt
helpviewer_keywords:
- CRBMap class
ms.assetid: 658e94dc-e835-4356-aed1-1513e1f66969
ms.openlocfilehash: 55d96bfd2c7b043bdbdc4c1ee1f329c9b77b9ca9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141054"
---
# <a name="crbmap-class"></a>Класс Крбмап

Этот класс представляет структуру сопоставления с помощью Red-Black двоичного дерева.

## <a name="syntax"></a>Синтаксис

```
template <typename K,
          typename V,
          class KTraits = CElementTraits<K>,
          class VTraits = CElementTraits<V>>
class CRBMap : public CRBTree<K, V, KTraits, VTraits>
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
|[Крбмап:: Крбмап](#crbmap)|Конструктор.|
|[Крбмап:: ~ Крбмап](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Крбмап:: Lookup](#lookup)|Вызывайте этот метод для поиска ключей или значений в `CRBMap` объекте.|
|[Крбмап:: Ремовекэй](#removekey)|Вызовите этот метод, чтобы удалить элемент из `CRBMap` объекта по заданному ключу.|
|[Крбмап:: SetAt](#setat)|Вызовите этот метод, чтобы вставить пару элементов в карту.|

## <a name="remarks"></a>Комментарии

`CRBMap` обеспечивает поддержку для массива сопоставления любого заданного типа, управляя упорядоченным массивом ключевых элементов и связанных с ними значений. Каждый ключ может иметь только одно связанное значение. Элементы (состоящие из ключа и значения) хранятся в виде двоичной древовидной структуры с помощью метода [крбмап:: SetAt](#setat) . Элементы можно удалить с помощью метода [крбмап:: ремовекэй](#removekey) , который удаляет элемент с заданным значением ключа.

Обход дерева становится возможным благодаря таким методам, как [крбтри:: жесеадпоситион](../../atl/reference/crbtree-class.md#getheadposition), [Крбтри:: GetNext](../../atl/reference/crbtree-class.md#getnext)и [крбтри:: жетнекствалуе](../../atl/reference/crbtree-class.md#getnextvalue).

Параметры *ктраитс* и *втраитс* являются признаками классов, которые содержат любой дополнительный код, необходимый для копирования или перемещения элементов.

`CRBMap` является производным от [крбтри](../../atl/reference/crbtree-class.md), который реализует двоичное дерево с помощью алгоритма Red-Black. [Крбмултимап](../../atl/reference/crbmultimap-class.md) — это вариант, допускающий несколько значений для каждого ключа. Он также является производным от `CRBTree` , и поэтому использует многие функции совместно с `CRBMap` .

Альтернатива и для `CRBMap` , и `CRBMultiMap` предлагается классом [CAtlMap](../../atl/reference/catlmap-class.md) . Если необходимо сохранить небольшое количество элементов, рекомендуется использовать класс [ксимплемап](../../atl/reference/csimplemap-class.md) .

Более подробное обсуждение различных классов коллекций, их функций и характеристик производительности см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[крбтри](../../atl/reference/crbtree-class.md)

`CRBMap`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="crbmapcrbmap"></a><a name="crbmap"></a> Крбмап:: Крбмап

Конструктор.

```
explicit CRBMap(size_t nBlockSize = 10) throw();
```

### <a name="parameters"></a>Параметры

*нблокксизе*<br/>
Размер блока.

### <a name="remarks"></a>Комментарии

Параметр *нблокксизе* — это мера объема памяти, выделенной, когда требуется новый элемент. Большие размеры блоков сокращают число вызовов подпрограмм выделения памяти, но используют больше ресурсов. По умолчанию выделяется место для 10 элементов за раз.

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#81](../../atl/codesnippet/cpp/crbmap-class_1.cpp)]

## <a name="crbmapcrbmap"></a><a name="dtor"></a> Крбмап:: ~ Крбмап

Деструктор

```
~CRBMap() throw();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы.

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

## <a name="crbmaplookup"></a><a name="lookup"></a> Крбмап:: Lookup

Вызывайте этот метод для поиска ключей или значений в `CRBMap` объекте.

```
bool Lookup(KINARGTYPE key, VOUTARGTYPE value) const throw(...);
const CPair* Lookup(KINARGTYPE key) const throw();
CPair* Lookup(KINARGTYPE key) throw();
```

### <a name="parameters"></a>Параметры

*key*<br/>
Задает ключ, определяющий элемент для поиска.

*value*<br/>
Переменная, принимающая искомое значение.

### <a name="return-value"></a>Возвращаемое значение

Первая форма метода возвращает значение true, если ключ найден; в противном случае — значение false. Вторая и третья формы возвращают указатель на [кпаир](crbtree-class.md#cpair_class).

### <a name="remarks"></a>Комментарии

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#82](../../atl/codesnippet/cpp/crbmap-class_2.cpp)]

## <a name="crbmapremovekey"></a><a name="removekey"></a> Крбмап:: Ремовекэй

Вызовите этот метод, чтобы удалить элемент из `CRBMap` объекта по заданному ключу.

```
bool RemoveKey(KINARGTYPE key) throw();
```

### <a name="parameters"></a>Параметры

*key*<br/>
Ключ, соответствующий паре элементов, которое необходимо удалить.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если ключ найден и удален, и false при сбое.

### <a name="remarks"></a>Комментарии

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#83](../../atl/codesnippet/cpp/crbmap-class_3.cpp)]

## <a name="crbmapsetat"></a><a name="setat"></a> Крбмап:: SetAt

Вызовите этот метод, чтобы вставить пару элементов в карту.

```
POSITION SetAt(
    KINARGTYPE key,
    VINARGTYPE value) throw(...);
```

### <a name="parameters"></a>Параметры

*key*<br/>
Значение ключа, добавляемое в `CRBMap` объект.

*value*<br/>
Значение, добавляемое в `CRBMap` объект.

### <a name="return-value"></a>Возвращаемое значение

Возвращает расположение пары элементов "ключ-значение" в `CRBMap` объекте.

### <a name="remarks"></a>Комментарии

`SetAt` заменяет существующий элемент, если найден соответствующий ключ. Если ключ не найден, создается новая пара "ключ-значение".

Сведения о других доступных методах см. в документации по базовому классу [крбтри](../../atl/reference/crbtree-class.md) .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#84](../../atl/codesnippet/cpp/crbmap-class_4.cpp)]

## <a name="see-also"></a>См. также раздел

[Класс Крбтри](../../atl/reference/crbtree-class.md)<br/>
[Класс CAtlMap](../../atl/reference/catlmap-class.md)<br/>
[Класс Крбмултимап](../../atl/reference/crbmultimap-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
