---
description: 'Дополнительные сведения о: Кмапстрингтуб Class'
title: Класс Кмапстрингтуб
ms.date: 11/04/2016
f1_keywords:
- CMapStringToOb
- AFXCOLL/CMapStringToOb
- AFXCOLL/CMapStringToOb::CMapStringToOb
- AFXCOLL/CMapStringToOb::GetCount
- AFXCOLL/CMapStringToOb::GetHashTableSize
- AFXCOLL/CMapStringToOb::GetNextAssoc
- AFXCOLL/CMapStringToOb::GetSize
- AFXCOLL/CMapStringToOb::GetStartPosition
- AFXCOLL/CMapStringToOb::HashKey
- AFXCOLL/CMapStringToOb::InitHashTable
- AFXCOLL/CMapStringToOb::IsEmpty
- AFXCOLL/CMapStringToOb::Lookup
- AFXCOLL/CMapStringToOb::LookupKey
- AFXCOLL/CMapStringToOb::RemoveAll
- AFXCOLL/CMapStringToOb::RemoveKey
- AFXCOLL/CMapStringToOb::SetAt
helpviewer_keywords:
- CMapStringToOb [MFC], CMapStringToOb
- CMapStringToOb [MFC], GetCount
- CMapStringToOb [MFC], GetHashTableSize
- CMapStringToOb [MFC], GetNextAssoc
- CMapStringToOb [MFC], GetSize
- CMapStringToOb [MFC], GetStartPosition
- CMapStringToOb [MFC], HashKey
- CMapStringToOb [MFC], InitHashTable
- CMapStringToOb [MFC], IsEmpty
- CMapStringToOb [MFC], Lookup
- CMapStringToOb [MFC], LookupKey
- CMapStringToOb [MFC], RemoveAll
- CMapStringToOb [MFC], RemoveKey
- CMapStringToOb [MFC], SetAt
ms.assetid: 09653980-b885-4f3a-8594-0aeb7f94c601
ms.openlocfilehash: 9bd5f47fbb85e67784e5bcb50029d9d9e48e5bb4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97207869"
---
# <a name="cmapstringtoob-class"></a>Класс Кмапстрингтуб

Класс коллекции словаря, который сопоставляет уникальные объекты `CString` с указателями `CObject` .

## <a name="syntax"></a>Синтаксис

```
class CMapStringToOb : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмапстрингтуб:: Кмапстрингтуб](#cmapstringtoob)|Конструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмапстрингтуб:: NOCOUNT](#getcount)|Возвращает число элементов в этой карте.|
|[Кмапстрингтуб:: Жесаштаблесизе](#gethashtablesize)|Определяет текущее количество элементов в хэш-таблице.|
|[Кмапстрингтуб:: Жетнекстассок](#getnextassoc)|Возвращает следующий элемент для итерации.|
|[Кмапстрингтуб:: DataSize](#getsize)|Возвращает число элементов в этой карте.|
|[Кмапстрингтуб:: Жетстартпоситион](#getstartposition)|Возвращает расположение первого элемента.|
|[Кмапстрингтуб:: Хашкэй](#hashkey)|Вычисляет хэш-значение указанного ключа.|
|[Кмапстрингтуб:: Инисаштабле](#inithashtable)|Инициализирует хэш-таблицу.|
|[Кмапстрингтуб:: IsEmpty](#isempty)|Проверяет условие на пустую карту (нет элементов).|
|[Кмапстрингтуб:: Lookup](#lookup)|Ищет указатель void на основе ключа указателя void. Значение указателя, а не сущность, на которое он указывает, используется для сравнения ключей.|
|[Кмапстрингтуб:: LookupKey](#lookupkey)|Возвращает ссылку на ключ, связанный с указанным значением ключа.|
|[Кмапстрингтуб:: RemoveAll](#removeall)|Удаляет все элементы из этой схемы.|
|[Кмапстрингтуб:: Ремовекэй](#removekey)|Удаляет элемент, указанный ключом.|
|[Кмапстрингтуб:: SetAt](#setat)|Вставляет элемент в карту; заменяет существующий элемент, если найден соответствующий ключ.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Кмапстрингтуб:: operator \[\]](#operator_at)|Вставляет элемент в Map — подстановку оператора для `SetAt` .|

## <a name="remarks"></a>Комментарии

После вставки `CString` -  `CObject*` пары (элемента) в карту можно эффективно получить или удалить пару, используя строку или `CString` значение в качестве ключа. Можно также выполнить итерацию по всем элементам на карте.

Переменная типа "расположение" используется для альтернативного доступа к записи во всех вариантах карт. Можно использовать точку для «запомнить» запись и выполнить итерацию по карте. Можно подумать, что эта итерация выполняется последовательно по значению ключа; Нет. Последовательность извлеченных элементов является неопределенной.

`CMapStringToOb` использует макрос `IMPLEMENT_SERIAL` для поддержки сериализации и записи элементов в дамп. Каждый элемент сериализуется в свою очередь, если схема хранится в архиве с перегруженным **<<** оператором вставки () или с `Serialize` функцией-членом.

Если требуется диагностический дамп отдельных элементов на карте ( `CString` значение и `CObject` содержимое), необходимо задать глубину контекста дампа в 1 или более.

При `CMapStringToOb` удалении объекта или удалении его элементов `CString` объекты и `CObject` указатели удаляются. Объекты, на которые ссылаются `CObject` указатели, не уничтожаются.

Наследование класса Map аналогично наследованию списка. Сведения о наследовании класса специального списка см. в статье [коллекции](../../mfc/collections.md) статей.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CMapStringToOb`

## <a name="requirements"></a>Требования

**Заголовок:** афксколл. h

## <a name="cmapstringtoobcmapstringtoob"></a><a name="cmapstringtoob"></a> Кмапстрингтуб:: Кмапстрингтуб

Конструирует пустое `CString` значение для `CObject*` отображения.

```
CMapStringToOb(INT_PTR nBlockSize = 10);
```

### <a name="parameters"></a>Параметры

*нблокксизе*<br/>
Задает гранулярность выделения памяти для расширения схемы.

### <a name="remarks"></a>Комментарии

По мере роста схемы память выделяется в единицах *нблокксизе* записей.

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb:: CMapStringToOb` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**Кмапптртоптр (INT_PTR** `nBlockSize` **= 10);**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**Кмапптртоворд (INT_PTR** `nBlockSize` **= 10);**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**Кмапстрингтоптр (INT_PTR** `nBlockSize` **= 10);**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**Кмапстрингтостринг (INT_PTR** `nBlockSize` **= 10);**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**Кмапвордтуб (INT_PTR** `nBlockSize` **= 10);**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**Мапвордтоптр (INT_PTR** `nBlockSize` **= 10);**|

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#63](../../mfc/codesnippet/cpp/cmapstringtoob-class_1.cpp)]

Список классов, используемых во всех примерах коллекции, см. в разделе [коблист:: коблист](../../mfc/reference/coblist-class.md#coblist) `CAge` .

## <a name="cmapstringtoobgetcount"></a><a name="getcount"></a> Кмапстрингтуб:: NOCOUNT

Определяет количество элементов на карте.

```
INT_PTR GetCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число элементов в этой карте.

### <a name="remarks"></a>Комментарии

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::GetCount` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**INT_PTR вычислить const ();**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**INT_PTR вычислить const ();**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**INT_PTR вычислить const ();**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**INT_PTR вычислить const ();**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**INT_PTR вычислить const ();**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**INT_PTR вычислить const ();**|

### <a name="example"></a>Пример

Список классов, используемых во всех примерах коллекции, см. в разделе [коблист:: коблист](../../mfc/reference/coblist-class.md#coblist) `CAge` .

[!code-cpp[NVC_MFCCollections#64](../../mfc/codesnippet/cpp/cmapstringtoob-class_2.cpp)]

## <a name="cmapstringtoobgethashtablesize"></a><a name="gethashtablesize"></a> Кмапстрингтуб:: Жесаштаблесизе

Определяет текущее количество элементов в хэш-таблице.

```
UINT GetHashTableSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает количество элементов в хэш-таблице.

### <a name="remarks"></a>Комментарии

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::GetHashTableSize` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**UINT Жесаштаблесизе () const;**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**UINT Жесаштаблесизе () const;**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**UINT Жесаштаблесизе () const;**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**UINT Жесаштаблесизе () const;**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**UINT Жесаштаблесизе () const;**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**UINT Жесаштаблесизе () const;**|

## <a name="cmapstringtoobgetnextassoc"></a><a name="getnextassoc"></a> Кмапстрингтуб:: Жетнекстассок

Извлекает элемент Map по адресу *рнекстпоситион*, а затем обновляет *рнекстпоситион* для ссылки на следующий элемент в сопоставлении.

```cpp
void GetNextAssoc(
    POSITION& rNextPosition,
    CString& rKey,
    CObject*& rValue) const;
```

### <a name="parameters"></a>Параметры

*рнекстпоситион*<br/>
Задает ссылку на значение, возвращенное предыдущим `GetNextAssoc` или `GetStartPosition` вызовом метода.

*ркэй*<br/>
Указывает возвращаемый ключ извлеченного элемента (строка).

*rValue*<br/>
Указывает возвращаемое значение извлеченного элемента ( `CObject` указатель). Дополнительные сведения об этом параметре см. в разделе "Примечания".

### <a name="remarks"></a>Комментарии

Эта функция наиболее полезна для прохода по всем элементам на карте. Обратите внимание, что последовательность позиций не обязательно совпадает с последовательностью значений ключа.

Если извлеченный элемент является последним в сопоставлении, то новое значение *рнекстпоситион* устанавливается в NULL.

Для параметра *rvalue* обязательно приведите тип объекта к типу **CObject \* &**, который требуется компилятору, как показано в следующем примере:

[!code-cpp[NVC_MFCCollections#65](../../mfc/codesnippet/cpp/cmapstringtoob-class_3.cpp)]

Это не относится `GetNextAssoc` к картам, основанным на шаблонах.

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::GetNextAssoc` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**void жетнекстассок (позиционирование&** *рнекстпоситион* **, void \* &** *ркэй* **, void \* &** *rvalue* **) const;**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**void жетнекстассок (позиционирование&** *рнекстпоситион* **, void \* &** *ркэй* **, Word&** *rvalue* **) const;**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**void жетнекстассок (позиционирование&** *рнекстпоситион* **, CString&** *ркэй* **, void \* &** *rvalue* **) const;**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**void жетнекстассок (позиционирование&** *рнекстпоситион* **, cstring&** *ркэй* **, CString&** *rvalue* **) const;**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**void жетнекстассок (позиционирование&** *рнекстпоситион* **, Word&** *ркэй* **, CObject \* &** *rvalue* **) const;**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**void жетнекстассок (позиционирование&** *рнекстпоситион* **, Word&** *ркэй* **, void \* &** *rvalue* **) const;**|

### <a name="example"></a>Пример

Список классов, используемых во всех примерах коллекции, см. в разделе [коблист:: коблист](../../mfc/reference/coblist-class.md#coblist) `CAge` .

[!code-cpp[NVC_MFCCollections#66](../../mfc/codesnippet/cpp/cmapstringtoob-class_4.cpp)]

Результаты этой программы выглядят следующим образом:

```Output
Lisa : a CAge at $4724 11
Marge : a CAge at $47A8 35
Homer : a CAge at $4766 36
Bart : a CAge at $45D4 13
```

## <a name="cmapstringtoobgetsize"></a><a name="getsize"></a> Кмапстрингтуб:: DataSize

Возвращает число элементов Map.

```
INT_PTR GetSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число элементов в сопоставлении.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы получить количество элементов в сопоставлении.

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::GetSize` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**INT_PTR-size () const;**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**INT_PTR-size () const;**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**INT_PTR-size () const;**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**INT_PTR-size () const;**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**INT_PTR-size () const;**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**INT_PTR-size () const;**|

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#67](../../mfc/codesnippet/cpp/cmapstringtoob-class_5.cpp)]

## <a name="cmapstringtoobgetstartposition"></a><a name="getstartposition"></a> Кмапстрингтуб:: Жетстартпоситион

Запускает итерацию Map, возвращая значение ПОЗИЦИЕЙ, которое можно передать в `GetNextAssoc` вызов.

```
POSITION GetStartPosition() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение положения, указывающее начальную точку для прохода по карте; или значение NULL, если схема пуста.

### <a name="remarks"></a>Комментарии

Последовательность итераций не является прогнозируемой. Таким образом, «первый элемент на карте» не имеет особой значимости.

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::GetStartPosition` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**Жетстартпоситион () const;**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**Жетстартпоситион () const;**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**Жетстартпоситион () const;**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**Жетстартпоситион () const;**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**Жетстартпоситион () const;**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**Жетстартпоситион () const;**|

### <a name="example"></a>Пример

См. пример для [кмапстрингтуб:: жетнекстассок](#getnextassoc).

## <a name="cmapstringtoobhashkey"></a><a name="hashkey"></a> Кмапстрингтуб:: Хашкэй

Вычисляет хэш-значение указанного ключа.

```
UINT HashKey(LPCTSTR key) const;
```

### <a name="parameters"></a>Параметры

*key*<br/>
Ключ, хэш-значение которого необходимо вычислить.

### <a name="return-value"></a>Возвращаемое значение

Хэш-значение ключа

### <a name="remarks"></a>Комментарии

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::HashKey` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**Uint хашкэй (void** <strong>\*</strong> `key` **) const;**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**Uint хашкэй (void** <strong>\*</strong> `key` **) const;**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**Uint хашкэй (LPCTSTR** `key` **) const;**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**Uint хашкэй (LPCTSTR** `key` **) const;**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**Uint хашкэй (Word** `key` **) const;**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**Uint хашкэй (Word** `key` **) const;**|

## <a name="cmapstringtoobinithashtable"></a><a name="inithashtable"></a> Кмапстрингтуб:: Инисаштабле

Инициализирует хэш-таблицу.

```cpp
void InitHashTable(
    UINT hashSize,
    BOOL bAllocNow = TRUE);
```

### <a name="parameters"></a>Параметры

*хашсизе*<br/>
Число записей в хэш-таблице.

*баллокнов*<br/>
Если значение — TRUE, при инициализации выделяется хэш-таблица. в противном случае таблица выделяется при необходимости.

### <a name="remarks"></a>Комментарии

Для лучшей производительности размер хэш-таблицы должен быть простым числом. Чтобы избежать конфликтов, размер должен быть примерно на 20% больше, чем самый большой ожидаемый набор данных.

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::InitHashTable` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**void инисаштабле (uint** `hashSize` **, bool** `bAllocNow` **= true);**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**void инисаштабле (uint** `hashSize` **, bool** `bAllocNow` **= true);**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**void инисаштабле (uint** `hashSize` **, bool** `bAllocNow` **= true);**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**void инисаштабле (uint** `hashSize` **, bool** `bAllocNow` **= true);**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**void инисаштабле (uint** `hashSize` **, bool** `bAllocNow` **= true);**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**void инисаштабле (uint** `hashSize` **, bool** `bAllocNow` **= true);**|

## <a name="cmapstringtoobisempty"></a><a name="isempty"></a> Кмапстрингтуб:: IsEmpty

Определяет, пуста ли схема.

```
BOOL IsEmpty() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если эта схема не содержит элементов; в противном случае — 0.

### <a name="example"></a>Пример

См. пример для [RemoveAll](#removeall).

### <a name="remarks"></a>Комментарии

В следующей таблице показаны другие функции элементов, аналогичные **кмапстрингтуб:: IsEmpty**.

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**BOOL-Empty () const;**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**BOOL-Empty () const;**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**BOOL-Empty () const;**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**BOOL-Empty () const;**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**BOOL-Empty () const;**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**BOOL-Empty () const;**|

## <a name="cmapstringtooblookup"></a><a name="lookup"></a> Кмапстрингтуб:: Lookup

Возвращает `CObject` указатель, основанный на `CString` значении.

```
BOOL Lookup(
    LPCTSTR key,
    CObject*& rValue) const;
```

### <a name="parameters"></a>Параметры

*key*<br/>
Задает ключ строки, определяющий элемент для поиска.

*rValue*<br/>
Указывает возвращаемое значение из просматриваемого элемента.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если элемент найден; в противном случае — 0.

### <a name="remarks"></a>Комментарии

`Lookup` использует алгоритм хэширования для быстрого поиска элемента Map с ключом, точно соответствующим ( `CString` value).

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::LookUp` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**Bool-Поиск (void** <strong>\*</strong> `key` **, void \* &** `rValue` **) const;**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**Bool-Поиск (void** <strong>\*</strong> `key` **, WORD&** `rValue` **) const;**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**Bool Lookup (LPCTSTR** `key` **, void \* &** `rValue` **) const;**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**Bool Lookup (LPCTSTR** `key` **, CString&** `rValue` **) const;**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**Bool Lookup (Word** `key` **, CObject \* &** `rValue` **) const;**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**Bool Lookup (слово** `key` **, void \* &** `rValue` **) const;**|

### <a name="example"></a>Пример

Список классов, используемых во всех примерах коллекции, см. в разделе [коблист:: коблист](../../mfc/reference/coblist-class.md#coblist) `CAge` .

[!code-cpp[NVC_MFCCollections#68](../../mfc/codesnippet/cpp/cmapstringtoob-class_6.cpp)]

## <a name="cmapstringtooblookupkey"></a><a name="lookupkey"></a> Кмапстрингтуб:: LookupKey

Возвращает ссылку на ключ, связанный с указанным значением ключа.

```
BOOL LookupKey(
    LPCTSTR key,
    LPCTSTR& rKey) const;
```

### <a name="parameters"></a>Параметры

*key*<br/>
Задает ключ строки, определяющий элемент для поиска.

*ркэй*<br/>
Ссылка на связанный ключ.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если ключ найден; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Использование ссылки на ключ является ненадежным, если используется после удаления связанного элемента из сопоставления или после уничтожения сопоставления.

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb:: LookupKey` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**Bool LookupKey (LPCTSTR** `key` **, LPCTSTR&** `rKey` **) const;**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**Bool LookupKey (LPCTSTR** `key` **, LPCTSTR&** `rKey` **) const;**|

## <a name="cmapstringtooboperator--"></a><a name="operator_at"></a> Кмапстрингтуб:: operator []

Удобное подстановка для `SetAt` функции-члена.

```
CObject*& operator[ ](lpctstr key);
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на указатель на `CObject` объект; или значение null, если схема пуста или *ключ* выходит за пределы диапазона.

### <a name="remarks"></a>Комментарии

Поэтому его можно использовать только в левой части оператора присваивания (l-значение). Если элемент Map с указанным ключом отсутствует, создается новый элемент.

Нет "правого" (r-Value), эквивалентного этому оператору, так как существует вероятность, что ключ не может быть найден на карте. Используйте `Lookup` функцию члена для получения элементов.

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::operator []` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|<strong>void \*& operator \[ ] (void \*</strong> `key` **\) ;**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**WORD& оператор \[ ] (void** <strong>\*</strong> `key` **\);**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**void \*& operator \[ ] (LPCTSTR** `key` **\) ;**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**CString&, оператор \[ ] (LPCTSTR** `key` **\);**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**CObject \*& operator \[ ] (Word** `key` **\) ;**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**void \*& operator \[ ] (Word** `key` **\) ;**|

### <a name="example"></a>Пример

Список классов, используемых во всех примерах коллекции, см. в разделе [коблист:: коблист](../../mfc/reference/coblist-class.md#coblist) `CAge` .

[!code-cpp[NVC_MFCCollections#72](../../mfc/codesnippet/cpp/cmapstringtoob-class_7.cpp)]

Результаты этой программы выглядят следующим образом:

```Output
Operator [] example: A CMapStringToOb with 2 elements
[Lisa] = a CAge at $4A02 11
[Bart] = a CAge at $497E 13
```

## <a name="cmapstringtoobremoveall"></a><a name="removeall"></a> Кмапстрингтуб:: RemoveAll

Удаляет все элементы из этой схемы и уничтожает `CString` Ключевые объекты.

```cpp
void RemoveAll();
```

### <a name="remarks"></a>Комментарии

`CObject`Объекты, на которые ссылается каждый ключ, не уничтожаются. `RemoveAll`Функция может вызвать утечку памяти, если не гарантировать, что объекты, на которые имеются ссылки, `CObject` будут уничтожены.

Функция работает правильно, если схема уже пуста.

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::RemoveAll` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**void RemoveAll ();**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**void RemoveAll ();**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**void RemoveAll ();**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**void RemoveAll ();**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**void RemoveAll ();**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**void RemoveAll ();**|

### <a name="example"></a>Пример

Список классов, используемых во всех примерах коллекции, см. в разделе [коблист:: коблист](../../mfc/reference/coblist-class.md#coblist) `CAge` .

[!code-cpp[NVC_MFCCollections#69](../../mfc/codesnippet/cpp/cmapstringtoob-class_8.cpp)]

## <a name="cmapstringtoobremovekey"></a><a name="removekey"></a> Кмапстрингтуб:: Ремовекэй

Выполняет поиск записи Map, соответствующей заданному ключу; Затем, если ключ найден, удаляет запись.

```
BOOL RemoveKey(LPCTSTR key);
```

### <a name="parameters"></a>Параметры

*key*<br/>
Указывает строку, используемую для уточняющего запроса таблицы.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если запись была найдена и успешно удалена; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Это может вызвать утечку памяти, если `CObject` объект не удаляется в других местах.

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::RemoveKey` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**Bool ремовекэй (void** <strong>\*</strong> `key` **);**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**Bool ремовекэй (void** <strong>\*</strong> `key` **);**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**Bool ремовекэй (LPCTSTR** `key` **);**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**Bool ремовекэй (LPCTSTR** `key` **);**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**Bool ремовекэй (Word** `key` **);**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**Bool ремовекэй (Word** `key` **);**|

### <a name="example"></a>Пример

Список классов, используемых во всех примерах коллекции, см. в разделе [коблист:: коблист](../../mfc/reference/coblist-class.md#coblist) `CAge` .

[!code-cpp[NVC_MFCCollections#70](../../mfc/codesnippet/cpp/cmapstringtoob-class_9.cpp)]

Результаты этой программы выглядят следующим образом:

```Output
RemoveKey example: A CMapStringToOb with 3 elements
[Marge] = a CAge at $49A0 35
[Homer] = a CAge at $495E 36
[Bart] = a CAge at $4634 13
```

## <a name="cmapstringtoobsetat"></a><a name="setat"></a> Кмапстрингтуб:: SetAt

Основной способ вставки элемента в карту.

```cpp
void SetAt(
    LPCTSTR key,
    CObject* newValue);
```

### <a name="parameters"></a>Параметры

*key*<br/>
Задает строку, которая является ключом нового элемента.

*newValue*<br/>
Задает `CObject` указатель, являющийся значением нового элемента.

### <a name="remarks"></a>Комментарии

Во-первых, ищется ключ. Если ключ найден, соответствующее значение изменяется. в противном случае создается новый элемент "ключ-значение".

В следующей таблице показаны другие функции элементов, аналогичные `CMapStringToOb::SetAt` .

|Класс|Функция-член|
|-----------|---------------------|
|[CMapPtrToPtr](../../mfc/reference/cmapptrtoptr-class.md)|**void SetAt (void** <strong>\*</strong> `key` **, void** <strong>\*</strong> `newValue` **);**|
|[CMapPtrToWord](../../mfc/reference/cmapptrtoword-class.md)|**void SetAt (void** <strong>\*</strong> `key` **, Слово** `newValue` **);**|
|[CMapStringToPtr](../../mfc/reference/cmapstringtoptr-class.md)|**void SetAt (LPCTSTR** `key` **, void** <strong>\*</strong> `newValue` **);**|
|[CMapStringToString](../../mfc/reference/cmapstringtostring-class.md)|**void SetAt (LPCTSTR** `key` **, LPCTSTR** `newValue` **);**|
|[CMapWordToOb](../../mfc/reference/cmapwordtoob-class.md)|**void SetAt (Word** `key` **, CObject** <strong>\*</strong> `newValue` **);**|
|[CMapWordToPtr](../../mfc/reference/cmapwordtoptr-class.md)|**void SetAt (Word** `key` **, void** <strong>\*</strong> `newValue` **);**|

### <a name="example"></a>Пример

Список классов, используемых во всех примерах коллекции, см. в разделе [коблист:: коблист](../../mfc/reference/coblist-class.md#coblist) `CAge` .

[!code-cpp[NVC_MFCCollections#71](../../mfc/codesnippet/cpp/cmapstringtoob-class_10.cpp)]

Результаты этой программы выглядят следующим образом:

```Output
before Lisa's birthday: A CMapStringToOb with 2 elements
[Lisa] = a CAge at $493C 11
[Bart] = a CAge at $4654 13
after Lisa's birthday: A CMapStringToOb with 2 elements
[Lisa] = a CAge at $49C0 12
[Bart] = a CAge at $4654 13
```

## <a name="see-also"></a>См. также раздел

[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кмапптртоптр](../../mfc/reference/cmapptrtoptr-class.md)<br/>
[Класс Кмапптртоворд](../../mfc/reference/cmapptrtoword-class.md)<br/>
[Класс Кмапстрингтоптр](../../mfc/reference/cmapstringtoptr-class.md)<br/>
[Класс Кмапстрингтостринг](../../mfc/reference/cmapstringtostring-class.md)<br/>
[Класс Кмапвордтуб](../../mfc/reference/cmapwordtoob-class.md)<br/>
[Класс Кмапвордтоптр](../../mfc/reference/cmapwordtoptr-class.md)
