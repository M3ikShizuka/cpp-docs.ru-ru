---
description: 'Дополнительные сведения о: Ксимплемап Class'
title: Класс Ксимплемап
ms.date: 11/04/2016
f1_keywords:
- CSimpleMap
- ATLSIMPCOLL/ATL::CSimpleMap
- ATLSIMPCOLL/ATL::CSimpleMap::_ArrayElementType
- ATLSIMPCOLL/ATL::CSimpleMap::_ArrayKeyType
- ATLSIMPCOLL/ATL::CSimpleMap::CSimpleMap
- ATLSIMPCOLL/ATL::CSimpleMap::Add
- ATLSIMPCOLL/ATL::CSimpleMap::FindKey
- ATLSIMPCOLL/ATL::CSimpleMap::FindVal
- ATLSIMPCOLL/ATL::CSimpleMap::GetKeyAt
- ATLSIMPCOLL/ATL::CSimpleMap::GetSize
- ATLSIMPCOLL/ATL::CSimpleMap::GetValueAt
- ATLSIMPCOLL/ATL::CSimpleMap::Lookup
- ATLSIMPCOLL/ATL::CSimpleMap::Remove
- ATLSIMPCOLL/ATL::CSimpleMap::RemoveAll
- ATLSIMPCOLL/ATL::CSimpleMap::RemoveAt
- ATLSIMPCOLL/ATL::CSimpleMap::ReverseLookup
- ATLSIMPCOLL/ATL::CSimpleMap::SetAt
- ATLSIMPCOLL/ATL::CSimpleMap::SetAtIndex
helpviewer_keywords:
- CSimpleMap class
ms.assetid: 61b06eb4-ae73-44b0-a305-0afb5a33e8b1
ms.openlocfilehash: 66640e3fcd325d59b82a10d98188a6fcd74ca79d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140625"
---
# <a name="csimplemap-class"></a>Класс Ксимплемап

Этот класс обеспечивает поддержку простого массива сопоставления.

## <a name="syntax"></a>Синтаксис

```
template <class TKey, class TVal, class TEqual = CSimpleMapEqualHelper<TKey, TVal>>
class CSimpleMap
```

#### <a name="parameters"></a>Параметры

*TKey*<br/>
Тип элемента Key.

*твал*<br/>
Тип элемента value.

*текуал*<br/>
Объект признака, определяющий проверку на равенство для элементов типа `T` .

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Ксимплемап:: _ArrayElementType](#_arrayelementtype)|Typedef для типа значения.|
|[Ксимплемап:: _ArrayKeyType](#_arraykeytype)|Typedef для типа ключа.|

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксимплемап:: Ксимплемап](#csimplemap)|Конструктор.|
|[Ксимплемап:: ~ Ксимплемап](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксимплемап:: Add](#add)|Добавляет ключ и связанное значение в массив сопоставления.|
|[Ксимплемап:: Финдкэй](#findkey)|Находит конкретный ключ.|
|[Ксимплемап:: Финдвал](#findval)|Находит определенное значение.|
|[Ксимплемап:: Жеткэйат](#getkeyat)|Извлекает указанный ключ.|
|[Ксимплемап:: DataSize](#getsize)|Возвращает количество записей в массиве сопоставлений.|
|[Ксимплемап:: Жетвалуеат](#getvalueat)|Извлекает указанное значение.|
|[Ксимплемап:: Lookup](#lookup)|Возвращает значение, связанное с заданным ключом.|
|[Ксимплемап:: Remove](#remove)|Удаляет ключ и совпадающее значение.|
|[Ксимплемап:: RemoveAll](#removeall)|Удаляет все ключи и значения.|
|[Ксимплемап:: RemoveAt](#removeat)|Удаляет указанный ключ и совпадающее значение.|
|[Ксимплемап:: Реверселукуп](#reverselookup)|Возвращает ключ, связанный с заданным значением.|
|[Ксимплемап:: SetAt](#setat)|Задает значение, связанное с заданным ключом.|
|[Ксимплемап:: Сетатиндекс](#setatindex)|Задает конкретный ключ и значение.|

## <a name="remarks"></a>Комментарии

`CSimpleMap` обеспечивает поддержку простого массива сопоставления любого заданного типа `T` , управления неупорядоченным массивом ключевых элементов и связанными с ними значениями.

Параметр `TEqual` предоставляет средства определения функции равенства для двух элементов типа `T` . Создавая класс, аналогичный [ксимплемапекуалхелпер](../../atl/reference/csimplemapequalhelper-class.md), можно изменить поведение проверки на равенство для любого заданного массива. Например, при работе с массивом указателей может быть полезно определить равенство в зависимости от значений, на которые ссылается указатель. Реализация по умолчанию использует **оператор = = ()**.

`CSimpleMap`И, и [ксимплеаррай](../../atl/reference/csimplearray-class.md) предоставляются для совместимости с предыдущими выпусками ATL, а более полные и эффективные реализации коллекций предоставляются [CAtlArray](../../atl/reference/catlarray-class.md) и [CAtlMap](../../atl/reference/catlmap-class.md).

В отличие от других коллекций карт в ATL и MFC этот класс реализуется с помощью простого массива, а поиск поиска требует линейного поиска. `CAtlMap` следует использовать, если массив содержит большое количество элементов.

## <a name="requirements"></a>Требования

**Заголовок:** атлсимпколл. h

## <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#91](../../atl/codesnippet/cpp/csimplemap-class_1.cpp)]

## <a name="csimplemapadd"></a><a name="add"></a> Ксимплемап:: Add

Добавляет ключ и связанное значение в массив сопоставления.

```
BOOL Add(const TKey& key, const TVal& val);
```

### <a name="parameters"></a>Параметры

*key*<br/>
Ключ.

*Val*<br/>
Связанное значение.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если ключ и значение были успешно добавлены; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Каждая добавленная пара ключ-значение приводит к освобождению и повторному выделению памяти массива сопоставления, чтобы гарантировать непрерывность хранения данных для каждого из них. То есть второй элемент key всегда следует за первым ключевым элементом в памяти и т. д.

## <a name="csimplemap_arrayelementtype"></a><a name="_arrayelementtype"></a> Ксимплемап:: _ArrayElementType

Typedef для типа ключа.

```
typedef TVal _ArrayElementType;
```

## <a name="csimplemap_arraykeytype"></a><a name="_arraykeytype"></a> Ксимплемап:: _ArrayKeyType

Typedef для типа значения.

```
typedef TKey _ArrayKeyType;
```

## <a name="csimplemapcsimplemap"></a><a name="csimplemap"></a> Ксимплемап:: Ксимплемап

Конструктор.

```
CSimpleMap();
```

### <a name="remarks"></a>Комментарии

Инициализирует элементы данных.

## <a name="csimplemapcsimplemap"></a><a name="dtor"></a> Ксимплемап:: ~ Ксимплемап

Деструктор

```
~CSimpleMap();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы.

## <a name="csimplemapfindkey"></a><a name="findkey"></a> Ксимплемап:: Финдкэй

Находит конкретный ключ.

```
int FindKey(const TKey& key) const;
```

### <a name="parameters"></a>Параметры

*key*<br/>
Ключ, который нужно найти.

### <a name="return-value"></a>Возвращаемое значение

Возвращает индекс ключа, если он найден, в противном случае возвращает значение-1.

## <a name="csimplemapfindval"></a><a name="findval"></a> Ксимплемап:: Финдвал

Находит определенное значение.

```
int FindVal(const TVal& val) const;
```

### <a name="parameters"></a>Параметры

*Val*<br/>
Значение, поиск которого следует выполнить.

### <a name="return-value"></a>Возвращаемое значение

Возвращает индекс значения, если он найден, в противном случае возвращает значение-1.

## <a name="csimplemapgetkeyat"></a><a name="getkeyat"></a> Ксимплемап:: Жеткэйат

Извлекает ключ по указанному индексу.

```
TKey& GetKeyAt(int nIndex) const;
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Индекс возвращаемого ключевого поля.

### <a name="return-value"></a>Возвращаемое значение

Возвращает ключ, на который ссылается *ниндекс*.

### <a name="remarks"></a>Комментарии

Индекс, переданный *ниндекс* , должен быть допустимым, чтобы возвращаемое значение было осмысленным.

## <a name="csimplemapgetsize"></a><a name="getsize"></a> Ксимплемап:: DataSize

Возвращает количество записей в массиве сопоставлений.

```
int GetSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает число записей (ключ и значение — одна запись) в массиве сопоставлений.

## <a name="csimplemapgetvalueat"></a><a name="getvalueat"></a> Ксимплемап:: Жетвалуеат

Извлекает значение по указанному индексу.

```
TVal& GetValueAt(int nIndex) const;
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Индекс возвращаемого значения.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение, на которое ссылается *ниндекс*.

### <a name="remarks"></a>Комментарии

Индекс, переданный *ниндекс* , должен быть допустимым, чтобы возвращаемое значение было осмысленным.

## <a name="csimplemaplookup"></a><a name="lookup"></a> Ксимплемап:: Lookup

Возвращает значение, связанное с заданным ключом.

```
TVal Lookup(const TKey& key) const;
```

### <a name="parameters"></a>Параметры

*key*<br/>
Ключ.

### <a name="return-value"></a>Возвращаемое значение

Возвращает связанное значение. Если соответствующий ключ не найден, возвращается значение NULL.

## <a name="csimplemapremove"></a><a name="remove"></a> Ксимплемап:: Remove

Удаляет ключ и совпадающее значение.

```
BOOL Remove(const TKey& key);
```

### <a name="parameters"></a>Параметры

*key*<br/>
Ключ.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если ключ и совпадающее значение были успешно удалены; в противном случае — значение FALSE.

## <a name="csimplemapremoveall"></a><a name="removeall"></a> Ксимплемап:: RemoveAll

Удаляет все ключи и значения.

```cpp
void RemoveAll();
```

### <a name="remarks"></a>Комментарии

Удаляет все ключи и значения из объекта массива сопоставлений.

## <a name="csimplemapremoveat"></a><a name="removeat"></a> Ксимплемап:: RemoveAt

Удаляет ключ и связанное с ним значение по указанному индексу.

```
BOOL RemoveAt(int nIndex);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Индекс ключа и связанного значения, которые необходимо удалить.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, значение FALSE, если указанный индекс является недопустимым.

## <a name="csimplemapreverselookup"></a><a name="reverselookup"></a> Ксимплемап:: Реверселукуп

Возвращает ключ, связанный с заданным значением.

```
TKey ReverseLookup(const TVal& val) const;
```

### <a name="parameters"></a>Параметры

*Val*<br/>
Значение.

### <a name="return-value"></a>Возвращаемое значение

Возвращает связанный ключ. Если соответствующий ключ не найден, возвращается значение NULL.

## <a name="csimplemapsetat"></a><a name="setat"></a> Ксимплемап:: SetAt

Задает значение, связанное с заданным ключом.

```
BOOL SetAt(const TKey& key, const TVal& val);
```

### <a name="parameters"></a>Параметры

*key*<br/>
Ключ.

*Val*<br/>
Новое присваиваемое значение.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если ключ был найден, и значение было успешно изменено, в противном случае — FALSE.

## <a name="csimplemapsetatindex"></a><a name="setatindex"></a> Ксимплемап:: Сетатиндекс

Задает ключ и значение по указанному индексу.

```
BOOL SetAtIndex(
    int nIndex,
    const TKey& key,
    const TVal& val);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Индекс, ссылающийся на пары ключей и значений, которые необходимо изменить.

*key*<br/>
Новый ключ.

*Val*<br/>
Новое значение.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE в случае успеха, значение FALSE, если индекс был недопустимым.

### <a name="remarks"></a>Комментарии

Обновляет как ключ, так и значение, на которые указывает *ниндекс*.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
