---
description: 'Дополнительные сведения о: Ксимплеаррай Class'
title: Класс Ксимплеаррай
ms.date: 11/04/2016
f1_keywords:
- CSimpleArray
- ATLSIMPCOLL/ATL::CSimpleArray
- ATLSIMPCOLL/ATL::CSimpleArray::CSimpleArray
- ATLSIMPCOLL/ATL::CSimpleArray::Add
- ATLSIMPCOLL/ATL::CSimpleArray::Find
- ATLSIMPCOLL/ATL::CSimpleArray::GetData
- ATLSIMPCOLL/ATL::CSimpleArray::GetSize
- ATLSIMPCOLL/ATL::CSimpleArray::Remove
- ATLSIMPCOLL/ATL::CSimpleArray::RemoveAll
- ATLSIMPCOLL/ATL::CSimpleArray::RemoveAt
- ATLSIMPCOLL/ATL::CSimpleArray::SetAtIndex
helpviewer_keywords:
- CSimpleArray class
ms.assetid: ee0c9f39-b61c-4c18-bc43-4eada21dca3a
ms.openlocfilehash: 95750662587c7ab47500a338c3ecd7e74a92eb34
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140794"
---
# <a name="csimplearray-class"></a>Класс Ксимплеаррай

Этот класс предоставляет методы для управления простым массивом.

## <a name="syntax"></a>Синтаксис

```
template <class T, class TEqual = CSimpleArrayEqualHelper<T>>
class CSimpleArray
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных для хранения в массиве.

*текуал*<br/>
Объект признака, определяющий проверку на равенство для элементов типа *T*.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксимплеаррай:: Ксимплеаррай](#csimplearray)|Конструктор для простого массива.|
|[Ксимплеаррай:: ~ Ксимплеаррай](#dtor)|Деструктор для простого массива.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксимплеаррай:: Add](#add)|Добавляет новый элемент в массив.|
|[Ксимплеаррай:: Find](#find)|Находит элемент в массиве.|
|[Ксимплеаррай:: GetData](#getdata)|Возвращает указатель на данные, хранящиеся в массиве.|
|[Ксимплеаррай:: DataSize](#getsize)|Возвращает количество элементов, хранящихся в массиве.|
|[Ксимплеаррай:: Remove](#remove)|Удаляет заданный элемент из массива.|
|[Ксимплеаррай:: RemoveAll](#removeall)|Удаляет все элементы из массива.|
|[Ксимплеаррай:: RemoveAt](#removeat)|Удаляет указанный элемент из массива.|
|[Ксимплеаррай:: Сетатиндекс](#setatindex)|Задает указанный элемент в массиве.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CSimpleArray::operator\[\]](#operator_at)|Получает элемент из массива.|
|[Ксимплеаррай:: operator =](#operator_eq)|Оператор присвоения.|

## <a name="remarks"></a>Комментарии

`CSimpleArray` предоставляет методы для создания и управления простым массивом любого заданного типа `T` .

Параметр `TEqual` предоставляет средства определения функции равенства для двух элементов типа `T` . Создавая класс, аналогичный [ксимплеаррайекуалхелпер](../../atl/reference/csimplearrayequalhelper-class.md), можно изменить поведение проверки на равенство для любого заданного массива. Например, при работе с массивом указателей может быть полезно определить равенство в зависимости от значений, на которые ссылается указатель. В реализации по умолчанию используется **оператор operator = ()**.

`CSimpleArray`И, и [ксимплемап](../../atl/reference/csimplemap-class.md) предназначены для небольшого количества элементов. [CAtlArray](../../atl/reference/catlarray-class.md) и [CAtlMap](../../atl/reference/catlmap-class.md) должны использоваться, если массив содержит большое количество элементов.

## <a name="requirements"></a>Требования

**Заголовок:** атлсимпколл. h

## <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#86](../../atl/codesnippet/cpp/csimplearray-class_1.cpp)]

## <a name="csimplearrayadd"></a><a name="add"></a> Ксимплеаррай:: Add

Добавляет новый элемент в массив.

```
BOOL Add(const T& t);
```

### <a name="parameters"></a>Параметры

*t*<br/>
Элемент, добавляемый в массив.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если элемент успешно добавлен в массив; в противном случае — значение FALSE.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#87](../../atl/codesnippet/cpp/csimplearray-class_2.cpp)]

## <a name="csimplearraycsimplearray"></a><a name="csimplearray"></a> Ксимплеаррай:: Ксимплеаррай

Конструктор для объекта массива.

```
CSimpleArray(const CSimpleArray<T, TEqual>& src);
CSimpleArray();
```

### <a name="parameters"></a>Параметры

*src*<br/>
Существующий объект `CSimpleArray`.

### <a name="remarks"></a>Комментарии

Инициализирует элементы данных, создает новый пустой `CSimpleArray` объект или копию существующего `CSimpleArray` объекта.

## <a name="csimplearraycsimplearray"></a><a name="dtor"></a> Ксимплеаррай:: ~ Ксимплеаррай

Деструктор

```
~CSimpleArray();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы.

## <a name="csimplearrayfind"></a><a name="find"></a> Ксимплеаррай:: Find

Находит элемент в массиве.

```
int Find(const T& t) const;
```

### <a name="parameters"></a>Параметры

*t*<br/>
Элемент, для которого необходимо выполнить поиск.

### <a name="return-value"></a>Возвращаемое значение

Возвращает индекс найденного элемента или значение-1, если элемент не найден.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#88](../../atl/codesnippet/cpp/csimplearray-class_3.cpp)]

## <a name="csimplearraygetdata"></a><a name="getdata"></a> Ксимплеаррай:: GetData

Возвращает указатель на данные, хранящиеся в массиве.

```
T* GetData() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на данные в массиве.

## <a name="csimplearraygetsize"></a><a name="getsize"></a> Ксимплеаррай:: DataSize

Возвращает количество элементов, хранящихся в массиве.

```
int GetSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает количество элементов, хранящихся в массиве.

## <a name="csimplearrayoperator-"></a><a name="operator_at"></a> Ксимплеаррай:: operator \[\]

Получает элемент из массива.

```
T& operator[](int nindex);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Индекс элемента.

### <a name="return-value"></a>Возвращаемое значение

Возвращает элемент массива, на который ссылается *ниндекс*.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#89](../../atl/codesnippet/cpp/csimplearray-class_4.cpp)]

## <a name="csimplearrayoperator-"></a><a name="operator_eq"></a> Ксимплеаррай:: operator =

Оператор присвоения.

```
CSimpleArray<T, TEqual>
& operator=(
    const CSimpleArray<T, TEqual>& src);
```

### <a name="parameters"></a>Параметры

*src*<br/>
Массив для копирования.

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на обновленный `CSimpleArray` объект.

### <a name="remarks"></a>Комментарии

Копирует все элементы из `CSimpleArray` объекта, на который ссылается *src* , в текущий объект массива, заменяя все существующие данные.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#90](../../atl/codesnippet/cpp/csimplearray-class_5.cpp)]

## <a name="csimplearrayremove"></a><a name="remove"></a> Ксимплеаррай:: Remove

Удаляет заданный элемент из массива.

```
BOOL Remove(const T& t);
```

### <a name="parameters"></a>Параметры

*t*<br/>
Элемент, который необходимо удалить из массива.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если элемент найден и удален; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

При удалении элемента оставшиеся элементы массива перенумеруются для заполнения пустого пространства.

## <a name="csimplearrayremoveall"></a><a name="removeall"></a> Ксимплеаррай:: RemoveAll

Удаляет все элементы из массива.

```cpp
void RemoveAll();
```

### <a name="remarks"></a>Комментарии

Удаляет все элементы, которые в данный момент хранятся в массиве.

## <a name="csimplearrayremoveat"></a><a name="removeat"></a> Ксимплеаррай:: RemoveAt

Удаляет указанный элемент из массива.

```
BOOL RemoveAtint nIndex);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Индекс, указывающий на удаляемый элемент.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если элемент был удален, и значение FALSE, если индекс был недопустимым.

### <a name="remarks"></a>Комментарии

При удалении элемента оставшиеся элементы массива перенумеруются для заполнения пустого пространства.

## <a name="csimplearraysetatindex"></a><a name="setatindex"></a> Ксимплеаррай:: Сетатиндекс

Задает указанный элемент в массиве.

```
BOOL SetAtIndex(
    int nIndex,
    const T& t);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Индекс элемента, который необходимо изменить.

*t*<br/>
Значение, присваиваемое указанному элементу.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE в случае успеха, значение FALSE, если индекс был недопустимым.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
