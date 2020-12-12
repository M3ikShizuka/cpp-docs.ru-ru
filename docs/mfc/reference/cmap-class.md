---
description: 'Дополнительные сведения о: Кмап Class'
title: Класс Кмап
ms.date: 11/04/2016
f1_keywords:
- CMap
- AFXTEMPL/CMap
- AFXTEMPL/CMap::CPair
- AFXTEMPL/CMap::CMap
- AFXTEMPL/CMap::GetCount
- AFXTEMPL/CMap::GetHashTableSize
- AFXTEMPL/CMap::GetNextAssoc
- AFXTEMPL/CMap::GetSize
- AFXTEMPL/CMap::GetStartPosition
- AFXTEMPL/CMap::InitHashTable
- AFXTEMPL/CMap::IsEmpty
- AFXTEMPL/CMap::Lookup
- AFXTEMPL/CMap::PGetFirstAssoc
- AFXTEMPL/CMap::PGetNextAssoc
- AFXTEMPL/CMap::PLookup
- AFXTEMPL/CMap::RemoveAll
- AFXTEMPL/CMap::RemoveKey
- AFXTEMPL/CMap::SetAt
helpviewer_keywords:
- CMap [MFC], CPair
- CMap [MFC], CMap
- CMap [MFC], GetCount
- CMap [MFC], GetHashTableSize
- CMap [MFC], GetNextAssoc
- CMap [MFC], GetSize
- CMap [MFC], GetStartPosition
- CMap [MFC], InitHashTable
- CMap [MFC], IsEmpty
- CMap [MFC], Lookup
- CMap [MFC], PGetFirstAssoc
- CMap [MFC], PGetNextAssoc
- CMap [MFC], PLookup
- CMap [MFC], RemoveAll
- CMap [MFC], RemoveKey
- CMap [MFC], SetAt
ms.assetid: 640a45ab-0993-4def-97ec-42cc78eb10b9
ms.openlocfilehash: ff88d205608cc87f06d28e6d2d4b647c35909efa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97207908"
---
# <a name="cmap-class"></a>Класс Кмап

Класс коллекции словарей, который сопоставляет уникальные ключи значениям.

## <a name="syntax"></a>Синтаксис

```
template<class KEY, class ARG_KEY, class VALUE, class ARG_VALUE>class CMap : public CObject
```

#### <a name="parameters"></a>Параметры

*KEY*<br/>
Класс объекта, используемый в качестве ключа для сопоставлений.

*ARG_KEY*<br/>
Тип данных, используемый для *ключевых* аргументов; обычно является ссылкой на *ключ*.

*VALUE*<br/>
Класс объекта, хранящегося на карте.

*ARG_VALUE*<br/>
Тип данных, используемый для аргументов *значения* ; обычно является ссылкой на *значение*.

## <a name="members"></a>Элементы

### <a name="public-structures"></a>Открытые структуры

|Имя|Описание|
|----------|-----------------|
|[Кмап:: Кпаир](#cpair)|Вложенная структура, содержащая значение ключа и значение связанного объекта.|

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмап:: Кмап](#cmap)|Конструирует коллекцию, которая сопоставляет ключи со значениями.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмап:: NOCOUNT](#getcount)|Возвращает число элементов в этой карте.|
|[Кмап:: Жесаштаблесизе](#gethashtablesize)|Возвращает количество элементов в хэш-таблице.|
|[Кмап:: Жетнекстассок](#getnextassoc)|Возвращает следующий элемент для итерации.|
|[Кмап:: DataSize](#getsize)|Возвращает число элементов в этой карте.|
|[Кмап:: Жетстартпоситион](#getstartposition)|Возвращает расположение первого элемента.|
|[Кмап:: Инисаштабле](#inithashtable)|Инициализирует хэш-таблицу и задает ее размер.|
|[Кмап:: IsEmpty](#isempty)|Проверяет условие на пустую карту (нет элементов).|
|[Кмап:: Lookup](#lookup)|Выполняет поиск значения, сопоставленного с заданным ключом.|
|[Кмап::P Жетфирстассок](#pgetfirstassoc)|Возвращает указатель на первый элемент.|
|[Кмап::P Жетнекстассок](#pgetnextassoc)|Возвращает указатель на следующий элемент для выполнения итерации.|
|[Кмап::P Поиск](#plookup)|Возвращает указатель на ключ, значение которого соответствует указанному значению.|
|[Кмап:: RemoveAll](#removeall)|Удаляет все элементы из этой схемы.|
|[Кмап:: Ремовекэй](#removekey)|Удаляет элемент, указанный ключом.|
|[Кмап:: SetAt](#setat)|Вставляет элемент в карту; заменяет существующий элемент, если найден соответствующий ключ.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Кмап:: operator \[\]](#operator_at)|Вставляет элемент в Map — подстановку оператора для `SetAt` .|

## <a name="remarks"></a>Комментарии

После вставки пары "ключ-значение" в карту можно эффективно получить или удалить пару с помощью ключа для доступа к ней. Можно также выполнить итерацию по всем элементам на карте.

Переменная позиции типа используется для альтернативного доступа к записям. Можно использовать точку для «запомнить» запись и выполнить итерацию по карте. Можно подумать, что эта итерация выполняется последовательно по значению ключа; Нет. Последовательность извлеченных элементов является неопределенной.

Некоторые функции элементов этого класса вызывают глобальные вспомогательные функции, которые необходимо настроить для большинства случаев использования `CMap` класса. См. раздел [вспомогательные методы класса Collection](../../mfc/reference/collection-class-helpers.md) в разделе макросы и глобальные **библиотеки справочника по MFC**.

`CMap` переопределяет [CObject:: Serialize](../../mfc/reference/cobject-class.md#serialize) для поддержки сериализации и дампа своих элементов. Если схема хранится в архиве с помощью `Serialize` , каждый элемент Map сериализуется по очереди. Реализация `SerializeElements` вспомогательной функции по умолчанию выполняет побитовую операцию записи. Сведения о сериализации элементов коллекций указателей, производных от `CObject` или других определяемых пользователем типов, см. [в разделе как создать Type-Safe коллекцию](../../mfc/how-to-make-a-type-safe-collection.md).

Если требуется диагностический дамп отдельных элементов на карте (ключи и значения), необходимо задать для контекста дампа значение 1 или больше.

При `CMap` удалении объекта или удалении его элементов ключи и значения удаляются.

Наследование класса Map аналогично наследованию списка. Сведения о наследовании класса специального списка см. в статье [коллекции](../../mfc/collections.md) статей.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CMap`

## <a name="requirements"></a>Требования

**Заголовок:** afxtempl.h

## <a name="cmapcmap"></a><a name="cmap"></a> Кмап:: Кмап

Конструирует пустую карту.

```
CMap(INT_PTR nBlockSize = 10);
```

### <a name="parameters"></a>Параметры

*нблокксизе*<br/>
Задает гранулярность выделения памяти для расширения схемы.

### <a name="remarks"></a>Комментарии

По мере роста схемы память выделяется в единицах *нблокксизе* записей.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#56](../../mfc/codesnippet/cpp/cmap-class_1.cpp)]

## <a name="cmapcpair"></a><a name="cpair"></a> Кмап:: Кпаир

Содержит значение ключа и значение связанного объекта.

### <a name="remarks"></a>Комментарии

Это вложенная структура в классе [кмап](../../mfc/reference/cmap-class.md).

Структура состоит из двух полей:

- `key` Фактическое значение типа ключа.

- `value` Значение связанного объекта.

Он используется для хранения возвращаемых значений из [кмап::P Lookup](#plookup), [Кмап::P жетфирстассок](#pgetfirstassoc)и [кмап::P жетнекстассок](#pgetnextassoc).

### <a name="example"></a>Пример

Пример использования см. в примере для [кмап::P Lookup](#plookup).

## <a name="cmapgetcount"></a><a name="getcount"></a> Кмап:: NOCOUNT

Возвращает количество элементов в сопоставлении.

```
INT_PTR GetCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число элементов.

### <a name="example"></a>Пример

См. пример для [кмап:: Lookup](#lookup).

## <a name="cmapgethashtablesize"></a><a name="gethashtablesize"></a> Кмап:: Жесаштаблесизе

Определяет количество элементов в хэш-таблице для схемы.

```
UINT GetHashTableSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число элементов в хэш-таблице.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#57](../../mfc/codesnippet/cpp/cmap-class_2.cpp)]

## <a name="cmapgetnextassoc"></a><a name="getnextassoc"></a> Кмап:: Жетнекстассок

Извлекает элемент Map в `rNextPosition` , а затем обновляет `rNextPosition` для ссылки на следующий элемент в сопоставлении.

```cpp
void GetNextAssoc(
    POSITION& rNextPosition,
    KEY& rKey,
    VALUE& rValue) const;
```

### <a name="parameters"></a>Параметры

*рнекстпоситион*<br/>
Задает ссылку на значение, возвращенное предыдущим `GetNextAssoc` или `GetStartPosition` вызовом метода.

*KEY*<br/>
Параметр шаблона, указывающий тип ключа на карте.

*ркэй*<br/>
Указывает возвращаемый ключ извлеченного элемента.

*VALUE*<br/>
Параметр шаблона, указывающий тип значения схемы.

*rValue*<br/>
Указывает возвращаемое значение извлеченного элемента.

### <a name="remarks"></a>Комментарии

Эта функция наиболее полезна для прохода по всем элементам на карте. Обратите внимание, что последовательность позиций не обязательно совпадает с последовательностью значений ключа.

Если извлеченный элемент является последним в сопоставлении, то новое значение *рнекстпоситион* устанавливается в NULL.

### <a name="example"></a>Пример

См. пример для [кмап:: SetAt](#setat).

## <a name="cmapgetsize"></a><a name="getsize"></a> Кмап:: DataSize

Возвращает число элементов Map.

```
INT_PTR GetSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число элементов в сопоставлении.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы получить количество элементов в сопоставлении.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#58](../../mfc/codesnippet/cpp/cmap-class_3.cpp)]

## <a name="cmapgetstartposition"></a><a name="getstartposition"></a> Кмап:: Жетстартпоситион

Запускает итерацию Map, возвращая значение ПОЗИЦИЕЙ, которое можно передать в `GetNextAssoc` вызов.

```
POSITION GetStartPosition() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение положения, указывающее начальную точку для прохода по карте; или значение NULL, если схема пуста.

### <a name="remarks"></a>Комментарии

Последовательность итераций не является прогнозируемой. Таким образом, «первый элемент на карте» не имеет особой значимости.

### <a name="example"></a>Пример

См. пример для [кмап:: SetAt](#setat).

## <a name="cmapinithashtable"></a><a name="inithashtable"></a> Кмап:: Инисаштабле

Инициализирует хэш-таблицу.

```cpp
void InitHashTable(UINT hashSize, BOOL  bAllocNow = TRUE);
```

### <a name="parameters"></a>Параметры

*хашсизе*<br/>
Число записей в хэш-таблице.

*баллокнов*<br/>
Если значение — TRUE, при инициализации выделяется хэш-таблица. в противном случае таблица выделяется при необходимости.

### <a name="remarks"></a>Комментарии

Для лучшей производительности размер хэш-таблицы должен быть простым числом. Чтобы избежать конфликтов, размер должен быть примерно на 20% больше, чем самый большой ожидаемый набор данных.

### <a name="example"></a>Пример

См. пример для [кмап:: Lookup](#lookup).

## <a name="cmapisempty"></a><a name="isempty"></a> Кмап:: IsEmpty

Определяет, пуста ли схема.

```
BOOL IsEmpty() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если эта схема не содержит элементов; в противном случае — 0.

### <a name="example"></a>Пример

См. пример для [кмап:: RemoveAll](#removeall).

## <a name="cmaplookup"></a><a name="lookup"></a> Кмап:: Lookup

Выполняет поиск значения, сопоставленного с заданным ключом.

```
BOOL Lookup(ARG_KEY key, VALUE& rValue) const;
```

### <a name="parameters"></a>Параметры

*ARG_KEY*<br/>
Параметр шаблона, указывающий тип значения *ключа* .

*key*<br/>
Задает ключ, определяющий элемент для поиска.

*VALUE*<br/>
Указывает тип значения, которое должно быть просмотрено.

*rValue*<br/>
Получает искомое значение.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если элемент найден; в противном случае — 0.

### <a name="remarks"></a>Комментарии

`Lookup` использует алгоритм хэширования для быстрого поиска элемента Map с ключом, точно соответствующим заданному ключу.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#58](../../mfc/codesnippet/cpp/cmap-class_3.cpp)]

## <a name="cmapoperator--"></a><a name="operator_at"></a> Кмап:: operator []

Удобное подстановка для `SetAt` функции-члена.

```
VALUE& operator[](arg_key key);
```

### <a name="parameters"></a>Параметры

*VALUE*<br/>
Параметр шаблона, указывающий тип значения сопоставлений.

*ARG_KEY*<br/>
Параметр шаблона, указывающий тип значения ключа.

*key*<br/>
Ключ, используемый для получения значения из схемы.

### <a name="remarks"></a>Комментарии

Поэтому его можно использовать только в левой части оператора присваивания (l-значение). Если элемент Map с указанным ключом отсутствует, создается новый элемент.

Нет "правого" (r-Value), эквивалентного этому оператору, так как существует вероятность, что ключ не может быть найден на карте. Используйте `Lookup` функцию члена для получения элементов.

### <a name="example"></a>Пример

См. пример для [кмап:: Lookup](#lookup).

## <a name="cmappgetfirstassoc"></a><a name="pgetfirstassoc"></a> Кмап::P Жетфирстассок

Возвращает первую запись объекта Map.

```
const CPair* PGetFirstAssoc() const;
CPair* PGetFirstAssoc();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на первую запись в сопоставлении; см. раздел [кмап:: кпаир](#cpair). Если на карте нет записей, значение равно NULL.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы вернуть указатель на первый элемент в объекте Map.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#59](../../mfc/codesnippet/cpp/cmap-class_4.cpp)]

## <a name="cmappgetnextassoc"></a><a name="pgetnextassoc"></a> Кмап::P Жетнекстассок

Извлекает элемент Map, на который указывает *пассокрек*.

```
const CPair *PGetNextAssoc(const CPair* pAssocRet) const;

CPair *PGetNextAssoc(const CPair* pAssocRet);
```

### <a name="parameters"></a>Параметры

*пассокрет*<br/>
Указывает на запись Map, возвращенную предыдущим вызовом [пжетнекстассок](#pgetnextassoc) или [Кмап::P жетфирстассок](#pgetfirstassoc) .

### <a name="return-value"></a>Возвращаемое значение

Указатель на следующую запись в сопоставлении; см. раздел [кмап:: кпаир](#cpair). Если элемент является последним в сопоставлении, значение равно NULL.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы выполнить итерацию всех элементов в сопоставлении. Получите первый элемент, вызвав метод `PGetFirstAssoc` , а затем выполните итерацию по карте с последовательными вызовами `PGetNextAssoc` .

### <a name="example"></a>Пример

См. пример для [кмап::P жетфирстассок](#pgetfirstassoc).

## <a name="cmapplookup"></a><a name="plookup"></a> Кмап::P Поиск

Находит значение, сопоставленное с заданным ключом.

```
const CPair* PLookup(ARG_KEY key) const;
CPair* PLookup(ARG_KEY key);
```

### <a name="parameters"></a>Параметры

*key*<br/>
Ключ для искомого элемента.

### <a name="return-value"></a>Возвращаемое значение

Указатель на структуру ключей; см. раздел [кмап:: кпаир](#cpair). Если совпадений не найдено, `CMap::PLookup` возвращает значение null.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы найти элемент Map с ключом, который точно соответствует заданному ключу.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#60](../../mfc/codesnippet/cpp/cmap-class_5.cpp)]

## <a name="cmapremoveall"></a><a name="removeall"></a> Кмап:: RemoveAll

Удаляет все значения из этой схемы, вызывая глобальную вспомогательную функцию `DestructElements` .

```cpp
void RemoveAll();
```

### <a name="remarks"></a>Комментарии

Функция работает правильно, если схема уже пуста.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#61](../../mfc/codesnippet/cpp/cmap-class_6.cpp)]

## <a name="cmapremovekey"></a><a name="removekey"></a> Кмап:: Ремовекэй

Выполняет поиск записи Map, соответствующей заданному ключу; Затем, если ключ найден, удаляет запись.

```
BOOL RemoveKey(ARG_KEY key);
```

### <a name="parameters"></a>Параметры

*ARG_KEY*<br/>
Параметр шаблона, указывающий тип ключа.

*key*<br/>
Ключ для удаляемого элемента.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если запись была найдена и успешно удалена; в противном случае — 0.

### <a name="remarks"></a>Комментарии

`DestructElements`Вспомогательная функция используется для удаления записи.

### <a name="example"></a>Пример

См. пример для [кмап:: SetAt](#setat).

## <a name="cmapsetat"></a><a name="setat"></a> Кмап:: SetAt

Основной способ вставки элемента в карту.

```cpp
void SetAt(ARG_KEY key, ARG_VALUE newValue);
```

### <a name="parameters"></a>Параметры

*ARG_KEY*<br/>
Параметр шаблона, указывающий тип параметра *ключа* .

*key*<br/>
Задает ключ нового элемента.

*ARG_VALUE*<br/>
Параметр шаблона, указывающий тип параметра *newValue* .

*newValue*<br/>
Задает значение нового элемента.

### <a name="remarks"></a>Комментарии

Во-первых, ищется ключ. Если ключ найден, соответствующее значение изменяется. в противном случае создается новая пара "ключ-значение".

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCollections#62](../../mfc/codesnippet/cpp/cmap-class_7.cpp)]

## <a name="see-also"></a>См. также раздел

[Пример СОБРАНий MFC](../../overview/visual-cpp-samples.md)<br/>
[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
