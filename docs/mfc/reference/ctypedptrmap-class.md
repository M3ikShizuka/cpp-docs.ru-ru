---
description: 'Дополнительные сведения о: Ктипедптрмап Class'
title: Класс Ктипедптрмап
ms.date: 11/04/2016
f1_keywords:
- CTypedPtrMap
- AFXTEMPL/CTypedPtrMap
- AFXTEMPL/CTypedPtrMap::GetNextAssoc
- AFXTEMPL/CTypedPtrMap::Lookup
- AFXTEMPL/CTypedPtrMap::RemoveKey
- AFXTEMPL/CTypedPtrMap::SetAt
helpviewer_keywords:
- CTypedPtrMap [MFC], GetNextAssoc
- CTypedPtrMap [MFC], Lookup
- CTypedPtrMap [MFC], RemoveKey
- CTypedPtrMap [MFC], SetAt
ms.assetid: 9f377385-c6e9-4471-8b40-8fe220c50164
ms.openlocfilehash: 25476a9195fe4a522ed31937dc1e2c5156ef6792
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344995"
---
# <a name="ctypedptrmap-class"></a>Класс Ктипедптрмап

Предоставляет типобезопасную "программу-оболочку" для объектов классов карты указателей `CMapPtrToPtr`, `CMapPtrToWord`, `CMapWordToPtr`и `CMapStringToPtr`.

## <a name="syntax"></a>Синтаксис

```
template<class BASE_CLASS, class KEY, class VALUE>
class CTypedPtrMap : public BASE_CLASS
```

#### <a name="parameters"></a>Параметры

*BASE_CLASS*<br/>
Базовый класс класса карт типизированного указателя; должен быть классом схемы указателя ( `CMapPtrToPtr` , `CMapPtrToWord` , `CMapWordToPtr` или `CMapStringToPtr` ).

*KEY*<br/>
Класс объекта, используемый в качестве ключа для сопоставлений.

*VALUE*<br/>
Класс объекта, хранящегося на карте.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ктипедптрмап:: Жетнекстассок](#getnextassoc)|Возвращает следующий элемент для итерации.|
|[Ктипедптрмап:: Lookup](#lookup)|Возвращает объект, `KEY` основанный на `VALUE` .|
|[Ктипедптрмап:: Ремовекэй](#removekey)|Удаляет элемент, указанный ключом.|
|[Ктипедптрмап:: SetAt](#setat)|Вставляет элемент в карту; заменяет существующий элемент, если найден соответствующий ключ.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Ктипедптрмап:: operator \[\]](#operator_at)|Вставляет элемент в карту.|

## <a name="remarks"></a>Комментарии

При использовании `CTypedPtrMap` средство проверки типов C++ помогает устранить ошибки, вызванные несовпадением типов указателей.

Поскольку все `CTypedPtrMap` функции являются встроенными, использование этого шаблона не оказывает существенного влияния на размер и скорость кода.

Дополнительные сведения об использовании `CTypedPtrMap` см. в статье [коллекции](../../mfc/collections.md) статей и [классы на основе шаблонов](../../mfc/template-based-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`BASE_CLASS`

`CTypedPtrMap`

## <a name="requirements"></a>Требования

**Заголовок:** afxtempl.h

## <a name="ctypedptrmapgetnextassoc"></a><a name="getnextassoc"></a> Ктипедптрмап:: Жетнекстассок

Извлекает элемент Map в `rNextPosition` , а затем обновляет `rNextPosition` для ссылки на следующий элемент в сопоставлении.

```cpp
void GetNextAssoc(
    POSITION& rPosition,
    KEY& rKey,
    VALUE& rValue) const;
```

### <a name="parameters"></a>Параметры

*rPosition*<br/>
Задает ссылку на значение, возвращаемое предыдущим `GetNextAssoc` вызовом или `BASE_CLASS` **:: жетстартпоситион** .

*KEY*<br/>
Параметр шаблона, указывающий тип ключей сопоставлений.

*ркэй*<br/>
Указывает возвращаемый ключ извлеченного элемента.

*VALUE*<br/>
Параметр шаблона, указывающий тип значений сопоставлений.

*rValue*<br/>
Указывает возвращаемое значение извлеченного элемента.

### <a name="remarks"></a>Комментарии

Эта функция наиболее полезна для прохода по всем элементам на карте. Обратите внимание, что последовательность позиций не обязательно совпадает с последовательностью значений ключа.

Если извлеченный элемент является последним в сопоставлении, новое значение устанавливается в значение `rNextPosition` null.

Эта встроенная функция вызывает `BASE_CLASS` **:: жетнекстассок**.

## <a name="ctypedptrmaplookup"></a><a name="lookup"></a> Ктипедптрмап:: Lookup

`Lookup` использует алгоритм хэширования для быстрого поиска элемента Map с ключом, точно соответствующим.

```
BOOL Lookup(BASE_CLASS ::BASE_ARG_KEY key, VALUE& rValue) const;
```

### <a name="parameters"></a>Параметры

*BASE_CLASS*<br/>
Параметр шаблона, указывающий базовый класс для класса этой схемы.

*key*<br/>
Ключ искомого элемента.

*VALUE*<br/>
Параметр шаблона, указывающий тип значений, хранящихся в этой карте.

*rValue*<br/>
Указывает возвращаемое значение извлеченного элемента.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если элемент найден; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Эта встроенная функция вызывает `BASE_CLASS` **:: Lookup**.

## <a name="ctypedptrmapoperator--"></a><a name="operator_at"></a> Ктипедптрмап:: operator []

Этот оператор можно использовать только с левой стороны оператора присваивания (l-значение).

```
VALUE& operator[ ](base_class ::base_arg_key key);
```

### <a name="parameters"></a>Параметры

*VALUE*<br/>
Параметр шаблона, указывающий тип значений, хранящихся в этой карте.

*BASE_CLASS*<br/>
Параметр шаблона, указывающий базовый класс для класса этой схемы.

*key*<br/>
Ключ элемента, который должен быть просмотрен или создан на карте.

### <a name="remarks"></a>Комментарии

Если элемент Map с указанным ключом отсутствует, создается новый элемент. Нет "правого" (r-Value), эквивалентного этому оператору, так как существует вероятность, что ключ не может быть найден на карте. Используйте `Lookup` функцию члена для получения элементов.

## <a name="ctypedptrmapremovekey"></a><a name="removekey"></a> Ктипедптрмап:: Ремовекэй

Эта функция члена вызывает `BASE_CLASS` **:: ремовекэй**.

```
BOOL RemoveKey(KEY key);
```

### <a name="parameters"></a>Параметры

*KEY*<br/>
Параметр шаблона, указывающий тип ключей сопоставлений.

*key*<br/>
Ключ для удаляемого элемента.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если запись была найдена и успешно удалена; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Более подробные примечания см. в разделе [кмапстрингтуб:: ремовекэй](../../mfc/reference/cmapstringtoob-class.md#removekey).

## <a name="ctypedptrmapsetat"></a><a name="setat"></a> Ктипедптрмап:: SetAt

Эта функция члена вызывает `BASE_CLASS` **:: SetAt**.

```cpp
void SetAt(KEY key, VALUE newValue);
```

### <a name="parameters"></a>Параметры

*KEY*<br/>
Параметр шаблона, указывающий тип ключей сопоставлений.

*key*<br/>
Задает значение ключа для значения newValue.

*newValue*<br/>
Указывает указатель на объект, являющийся значением нового элемента.

### <a name="remarks"></a>Комментарии

Более подробные примечания см. в разделе [кмапстрингтуб:: SetAt](../../mfc/reference/cmapstringtoob-class.md#setat).

## <a name="see-also"></a>См. также раздел

[Пример СОБРАНий MFC](../../overview/visual-cpp-samples.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кмапптртоптр](../../mfc/reference/cmapptrtoptr-class.md)<br/>
[Класс Кмапптртоворд](../../mfc/reference/cmapptrtoword-class.md)<br/>
[Класс Кмапвордтоптр](../../mfc/reference/cmapwordtoptr-class.md)<br/>
[Класс Кмапстрингтоптр](../../mfc/reference/cmapstringtoptr-class.md)
