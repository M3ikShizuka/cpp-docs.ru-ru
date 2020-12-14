---
description: 'Дополнительные сведения о: Кмфкфилтерчунквалуеимпл Class'
title: Класс CMFCFilterChunkValueImpl
ms.date: 11/04/2016
f1_keywords:
- CMFCFilterChunkValueImpl
- AFXWIN/CMFCFilterChunkValueImpl
- AFXWIN/CMFCFilterChunkValueImpl::CMFCFilterChunkValueImpl
- AFXWIN/CMFCFilterChunkValueImpl::Clear
- AFXWIN/CMFCFilterChunkValueImpl::CopyChunk
- AFXWIN/CMFCFilterChunkValueImpl::CopyFrom
- AFXWIN/CMFCFilterChunkValueImpl::GetChunkGUID
- AFXWIN/CMFCFilterChunkValueImpl::GetChunkPID
- AFXWIN/CMFCFilterChunkValueImpl::GetChunkType
- AFXWIN/CMFCFilterChunkValueImpl::GetString
- AFXWIN/CMFCFilterChunkValueImpl::GetValue
- AFXWIN/CMFCFilterChunkValueImpl::GetValueNoAlloc
- AFXWIN/CMFCFilterChunkValueImpl::IsValid
- AFXWIN/CMFCFilterChunkValueImpl::SetBoolValue
- AFXWIN/CMFCFilterChunkValueImpl::SetDwordValue
- AFXWIN/CMFCFilterChunkValueImpl::SetFileTimeValue
- AFXWIN/CMFCFilterChunkValueImpl::SetInt64Value
- AFXWIN/CMFCFilterChunkValueImpl::SetIntValue
- AFXWIN/CMFCFilterChunkValueImpl::SetLongValue
- AFXWIN/CMFCFilterChunkValueImpl::SetSystemTimeValue
- AFXWIN/CMFCFilterChunkValueImpl::SetTextValue
- AFXWIN/CMFCFilterChunkValueImpl::SetChunk
helpviewer_keywords:
- CMFCFilterChunkValueImpl [MFC], CMFCFilterChunkValueImpl
- CMFCFilterChunkValueImpl [MFC], Clear
- CMFCFilterChunkValueImpl [MFC], CopyChunk
- CMFCFilterChunkValueImpl [MFC], CopyFrom
- CMFCFilterChunkValueImpl [MFC], GetChunkGUID
- CMFCFilterChunkValueImpl [MFC], GetChunkPID
- CMFCFilterChunkValueImpl [MFC], GetChunkType
- CMFCFilterChunkValueImpl [MFC], GetString
- CMFCFilterChunkValueImpl [MFC], GetValue
- CMFCFilterChunkValueImpl [MFC], GetValueNoAlloc
- CMFCFilterChunkValueImpl [MFC], IsValid
- CMFCFilterChunkValueImpl [MFC], SetBoolValue
- CMFCFilterChunkValueImpl [MFC], SetDwordValue
- CMFCFilterChunkValueImpl [MFC], SetFileTimeValue
- CMFCFilterChunkValueImpl [MFC], SetInt64Value
- CMFCFilterChunkValueImpl [MFC], SetIntValue
- CMFCFilterChunkValueImpl [MFC], SetLongValue
- CMFCFilterChunkValueImpl [MFC], SetSystemTimeValue
- CMFCFilterChunkValueImpl [MFC], SetTextValue
- CMFCFilterChunkValueImpl [MFC], SetChunk
ms.assetid: 3c833f23-5b88-4d08-9e09-ca6a8aec88bf
ms.openlocfilehash: f2db7fdf6d6d24cb906b3190d34310e1f6724194
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97265471"
---
# <a name="cmfcfilterchunkvalueimpl-class"></a>Класс CMFCFilterChunkValueImpl

Это класс, который упрощает логику пар "блок-значения" и "значение свойства".

## <a name="syntax"></a>Синтаксис

```
class CMFCFilterChunkValueImpl : public ATL::IFilterChunkValue;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкфилтерчунквалуеимпл:: ~ Кмфкфилтерчунквалуеимпл](#_dtorcmfcfilterchunkvalueimpl)|Разструктура объекта.|
|[Кмфкфилтерчунквалуеимпл:: Кмфкфилтерчунквалуеимпл](#cmfcfilterchunkvalueimpl)|Создает объект.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкфилтерчунквалуеимпл:: Clear](#clear)|Очищает Чунквалуе.|
|[Кмфкфилтерчунквалуеимпл:: CopyChunk](#copychunk)|Копирует этот блок в структуру, описывающую характеристики фрагмента.|
|[Кмфкфилтерчунквалуеимпл:: CopyFrom](#copyfrom)|Инициализирует это значение блока из другого значения.|
|[Кмфкфилтерчунквалуеимпл:: Жетчункгуид](#getchunkguid)|Извлекает идентификатор GUID фрагмента.|
|[Кмфкфилтерчунквалуеимпл:: Жетчункпид](#getchunkpid)|Извлекает идентификатор PID блока (ИД свойства).|
|[Кмфкфилтерчунквалуеимпл:: Жетчунктипе](#getchunktype)|Возвращает тип блока.|
|[Кмфкфилтерчунквалуеимпл:: GetString](#getstring)|Извлекает строковое значение.|
|[Кмфкфилтерчунквалуеимпл:: GetValue](#getvalue)|Получает значение в виде выделенного пропвариант.|
|[Кмфкфилтерчунквалуеимпл:: Жетвалуеноаллок](#getvaluenoalloc)|Возвращает значение без выделения (внутреннее значение).|
|[Кмфкфилтерчунквалуеимпл:: IsValid](#isvalid)|Проверяет, является ли это значение свойства допустимым или нет.|
|[Кмфкфилтерчунквалуеимпл:: SetBoolValue](#setboolvalue)|Перегружен. Устанавливает свойство по ключу на логическое значение.|
|[Кмфкфилтерчунквалуеимпл:: Сетдвордвалуе](#setdwordvalue)|Устанавливает свойство по ключу в DWORD.|
|[Кмфкфилтерчунквалуеимпл:: Сетфилетимевалуе](#setfiletimevalue)|Задает свойство по ключу для значения FILETIME.|
|[Кмфкфилтерчунквалуеимпл:: SetInt64Value](#setint64value)|Устанавливает свойство по ключу для типа Int64.|
|[Кмфкфилтерчунквалуеимпл:: Сетинтвалуе](#setintvalue)|Задает свойство по ключу для типа int.|
|[Кмфкфилтерчунквалуеимпл:: Сетлонгвалуе](#setlongvalue)|Устанавливает свойство по ключу в значение LONG.|
|[Кмфкфилтерчунквалуеимпл:: Сетсистемтимевалуе](#setsystemtimevalue)|Задает свойство по ключу для SystemTime.|
|[Кмфкфилтерчунквалуеимпл:: Сеттекствалуе](#settextvalue)|Задает свойство по ключу для строки в Юникоде.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кмфкфилтерчунквалуеимпл:: Сетчунк](#setchunk)|Вспомогательная функция, которая задает общие свойства блока.|

## <a name="remarks"></a>Комментарии

Чтобы использовать, просто создайте класс Кмфкфилтерчунквалуеимпл нужного типа.

Пример

Кмфкфилтерчунквалуеимпл фрагмент;

HR = фрагмент. SetBoolValue (PKEY_IsAttachment, true);

или

HR = фрагмент. Сетфилетимевалуе (PKEY_ItemDate, Фтластмодифиед);

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`ATL::IFilterChunkValue`

[кмфкфилтерчунквалуеимпл](../../mfc/reference/cmfcfilterchunkvalueimpl-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxwin.h

## <a name="cmfcfilterchunkvalueimplclear"></a><a name="clear"></a> Кмфкфилтерчунквалуеимпл:: Clear

Очищает Чунквалуе.

```cpp
void Clear();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplcmfcfilterchunkvalueimpl"></a><a name="cmfcfilterchunkvalueimpl"></a> Кмфкфилтерчунквалуеимпл:: Кмфкфилтерчунквалуеимпл

Создает объект.

```
CMFCFilterChunkValueImpl();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplcmfcfilterchunkvalueimpl"></a><a name="_dtorcmfcfilterchunkvalueimpl"></a> Кмфкфилтерчунквалуеимпл:: ~ Кмфкфилтерчунквалуеимпл

Разструктура объекта.

```
virtual ~CMFCFilterChunkValueImpl();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplcopychunk"></a><a name="copychunk"></a> Кмфкфилтерчунквалуеимпл:: CopyChunk

Копирует этот блок в структуру, описывающую характеристики фрагмента.

```
HRESULT CopyChunk(STAT_CHUNK* pStatChunk);
```

### <a name="parameters"></a>Параметры

*пстатчунк*<br/>
Указатель на целевое значение, описывающее характеристики фрагмента.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplcopyfrom"></a><a name="copyfrom"></a> Кмфкфилтерчунквалуеимпл:: CopyFrom

Инициализирует это значение блока из другого значения.

```cpp
void CopyFrom (IFilterChunkValue* pValue);
```

### <a name="parameters"></a>Параметры

*pValue*<br/>
Указывает исходное значение, из которого производится копирование.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplgetchunkguid"></a><a name="getchunkguid"></a> Кмфкфилтерчунквалуеимпл:: Жетчункгуид

Извлекает идентификатор GUID фрагмента.

```
REFGUID GetChunkGUID() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на идентификатор GUID, определяющий фрагмент.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplgetchunkpid"></a><a name="getchunkpid"></a> Кмфкфилтерчунквалуеимпл:: Жетчункпид

Извлекает идентификатор PID блока (ИД свойства).

```
DWORD GetChunkPID() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение типа DWORD, содержащее идентификатор свойства.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplgetchunktype"></a><a name="getchunktype"></a> Кмфкфилтерчунквалуеимпл:: Жетчунктипе

Извлекает тип блока.

```
CHUNKSTATE GetChunkType() const;
```

### <a name="return-value"></a>Возвращаемое значение

Перечислимое значение ЧУНКСТАТЕ, которое указывает, является ли текущий фрагмент свойством текстового типа или свойством типа значения.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplgetstring"></a><a name="getstring"></a> Кмфкфилтерчунквалуеимпл:: GetString

Извлекает строковое значение.

```
CString &GetString();
```

### <a name="return-value"></a>Возвращаемое значение

Строка, содержащая значение блока.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplgetvalue"></a><a name="getvalue"></a> Кмфкфилтерчунквалуеимпл:: GetValue

Получает значение в виде выделенного пропвариант.

```
HRESULT GetValue(PROPVARIANT** ppPropVariant);
```

### <a name="parameters"></a>Параметры

*пппропвариант*<br/>
При возврате функции этот параметр содержит значение блока.

### <a name="return-value"></a>Возвращаемое значение

S_OK, если ПРОПВАРИАНТ был выделен успешно и значение фрагмента было успешно скопировано в *пппропвариант*; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplgetvaluenoalloc"></a><a name="getvaluenoalloc"></a> Кмфкфилтерчунквалуеимпл:: Жетвалуеноаллок

Возвращает невыделенное (внутреннее значение) значение.

```
PROPVARIANT GetValueNoAlloc ();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает текущее значение блока.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplisvalid"></a><a name="isvalid"></a> Кмфкфилтерчунквалуеимпл:: IsValid

Проверяет, является ли это значение свойства допустимым или нет.

```
BOOL IsValid() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если текущее значение блока является допустимым; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplsetboolvalue"></a><a name="setboolvalue"></a> Кмфкфилтерчунквалуеимпл:: SetBoolValue

Перегружен. Устанавливает свойство по ключу на логическое значение.

```
HRESULT SetBoolValue(
    REFPROPERTYKEY pkey,
    BOOL bVal,
    CHUNKSTATE chunkType = CHUNK_VALUE,
    LCID locale = 0,
    DWORD cwcLenSource = 0,
    DWORD cwcStartSource = 0,
    CHUNK_BREAKTYPE chunkBreakType = CHUNK_NO_BREAK);

HRESULT SetBoolValue(
    REFPROPERTYKEY pkey,
    VARIANT_BOOL bVal,
    CHUNKSTATE chunkType = CHUNK_VALUE,
    LCID locale = 0,
    DWORD cwcLenSource = 0,
    DWORD cwcStartSource = 0,
    CHUNK_BREAKTYPE chunkBreakType = CHUNK_NO_BREAK);
```

### <a name="parameters"></a>Параметры

*PKEY*<br/>
Указывает ключ свойства.

*бвал*<br/>
Задает заданное значение фрагмента.

*чунктипе*<br/>
Флаги указывают, содержит ли этот блок тип Text-Type или свойство значения. Значения флагов берутся из перечисления ЧУНКСТАТЕ.

*locale*<br/>
Язык и подязык, связанные с фрагментом текста. Языковой стандарт блока данных используется индексаторами документов для выполнения правильного разбиения текста на слова. Если фрагмент не является ни текстовым типом, ни типом значения с типом данных VT_LPWSTR, VT_LPSTR или VT_BSTR, это поле игнорируется.

*квкленсаурце*<br/>
Длина в символах исходного текста, из которого был получен текущий фрагмент. Нулевое значение обозначает соответствие символов по символам между исходным текстом и производным текстом. Ненулевое значение означает, что прямая корреспонденция не существует.

*квкстартсаурце*<br/>
Смещение, с которого исходный текст для производного фрагмента начинается в исходном блоке.

*чункбреактипе*<br/>
Тип разрыва, разделяющий предыдущий фрагмент из текущего фрагмента. Значения из перечисления CHUNK_BREAKTYPE.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplsetchunk"></a><a name="setchunk"></a> Кмфкфилтерчунквалуеимпл:: Сетчунк

Вспомогательная функция, которая задает общие свойства блока.

```
HRESULT SetChunk(
    REFPROPERTYKEY pkey,
    CHUNKSTATE chunkType=CHUNK_VALUE,
    LCID locale=0,
    DWORD cwcLenSource=0,
    DWORD cwcStartSource=0,
    CHUNK_BREAKTYPE chunkBreakType=CHUNK_NO_BREAK);
```

### <a name="parameters"></a>Параметры

*PKEY*<br/>
Указывает ключ свойства.

*чунктипе*<br/>
Флаги указывают, содержит ли этот блок тип Text-Type или свойство значения. Значения флагов берутся из перечисления ЧУНКСТАТЕ.

*locale*<br/>
Язык и подязык, связанные с фрагментом текста. Языковой стандарт блока данных используется индексаторами документов для выполнения правильного разбиения текста на слова. Если фрагмент не является ни текстовым типом, ни типом значения с типом данных VT_LPWSTR, VT_LPSTR или VT_BSTR, это поле игнорируется.

*квкленсаурце*<br/>
Длина в символах исходного текста, из которого был получен текущий фрагмент. Нулевое значение обозначает соответствие символов по символам между исходным текстом и производным текстом. Ненулевое значение означает, что прямая корреспонденция не существует.

*квкстартсаурце*<br/>
Смещение, с которого исходный текст для производного фрагмента начинается в исходном блоке.

*чункбреактипе*<br/>
Тип разрыва, разделяющий предыдущий фрагмент из текущего фрагмента. Значения из перечисления CHUNK_BREAKTYPE.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplsetdwordvalue"></a><a name="setdwordvalue"></a> Кмфкфилтерчунквалуеимпл:: Сетдвордвалуе

Задайте для свойства Key значение DWORD.

```
HRESULT SetDwordValue(
    REFPROPERTYKEY pkey,
    DWORD dwVal,
    CHUNKSTATE chunkType = CHUNK_VALUE,
    LCID locale = 0,
    DWORD cwcLenSource = 0,
    DWORD cwcStartSource = 0,
    CHUNK_BREAKTYPE chunkBreakType = CHUNK_NO_BREAK);
```

### <a name="parameters"></a>Параметры

*PKEY*<br/>
Указывает ключ свойства.

*дввал*<br/>
Задает заданное значение фрагмента.

*чунктипе*<br/>
Флаги указывают, содержит ли этот блок тип Text-Type или свойство значения. Значения флагов берутся из перечисления ЧУНКСТАТЕ.

*locale*<br/>
Язык и подязык, связанные с фрагментом текста. Языковой стандарт блока данных используется индексаторами документов для выполнения правильного разбиения текста на слова. Если фрагмент не является ни текстовым типом, ни типом значения с типом данных VT_LPWSTR, VT_LPSTR или VT_BSTR, это поле игнорируется.

*квкленсаурце*<br/>
Длина в символах исходного текста, из которого был получен текущий фрагмент. Нулевое значение обозначает соответствие символов по символам между исходным текстом и производным текстом. Ненулевое значение означает, что прямая корреспонденция не существует.

*квкстартсаурце*<br/>
Смещение, с которого исходный текст для производного фрагмента начинается в исходном блоке.

*чункбреактипе*<br/>
Тип разрыва, разделяющий предыдущий фрагмент из текущего фрагмента. Значения из перечисления CHUNK_BREAKTYPE.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplsetfiletimevalue"></a><a name="setfiletimevalue"></a> Кмфкфилтерчунквалуеимпл:: Сетфилетимевалуе

Присвойте свойству Key значение FILETIME.

```
HRESULT SetFileTimeValue(
    REFPROPERTYKEY pkey,
    FILETIME dtVal,
    CHUNKSTATE chunkType = CHUNK_VALUE,
    LCID locale = 0,
    DWORD cwcLenSource = 0,
    DWORD cwcStartSource = 0,
    CHUNK_BREAKTYPE chunkBreakType = CHUNK_NO_BREAK);
```

### <a name="parameters"></a>Параметры

*PKEY*<br/>
Указывает ключ свойства.

*дтвал*<br/>
Задает заданное значение фрагмента.

*чунктипе*<br/>
Флаги указывают, содержит ли этот блок тип Text-Type или свойство значения. Значения флагов берутся из перечисления ЧУНКСТАТЕ.

*locale*<br/>
Язык и подязык, связанные с фрагментом текста. Языковой стандарт блока данных используется индексаторами документов для выполнения правильного разбиения текста на слова. Если фрагмент не является ни текстовым типом, ни типом значения с типом данных VT_LPWSTR, VT_LPSTR или VT_BSTR, это поле игнорируется.

*квкленсаурце*<br/>
Длина в символах исходного текста, из которого был получен текущий фрагмент. Нулевое значение обозначает соответствие символов по символам между исходным текстом и производным текстом. Ненулевое значение означает, что прямая корреспонденция не существует.

*квкстартсаурце*<br/>
Смещение, с которого исходный текст для производного фрагмента начинается в исходном блоке.

*чункбреактипе*<br/>
Тип разрыва, разделяющий предыдущий фрагмент из текущего фрагмента. Значения из перечисления CHUNK_BREAKTYPE.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplsetint64value"></a><a name="setint64value"></a> Кмфкфилтерчунквалуеимпл:: SetInt64Value

Присвойте свойству по ключу значение Int64.

```
HRESULT SetInt64Value(
    REFPROPERTYKEY pkey,
    __int64 nVal,
    CHUNKSTATE chunkType = CHUNK_VALUE,
    LCID locale = 0,
    DWORD cwcLenSource = 0,
    DWORD cwcStartSource = 0,
    CHUNK_BREAKTYPE chunkBreakType = CHUNK_NO_BREAK);
```

### <a name="parameters"></a>Параметры

*PKEY*<br/>
Указывает ключ свойства.

*Непредвиденное nval*<br/>
Задает заданное значение фрагмента.

*чунктипе*<br/>
Флаги указывают, содержит ли этот блок тип Text-Type или свойство значения. Значения флагов берутся из перечисления ЧУНКСТАТЕ.

*locale*<br/>
Язык и подязык, связанные с фрагментом текста. Языковой стандарт блока данных используется индексаторами документов для выполнения правильного разбиения текста на слова. Если фрагмент не является ни текстовым типом, ни типом значения с типом данных VT_LPWSTR, VT_LPSTR или VT_BSTR, это поле игнорируется.

*квкленсаурце*<br/>
Длина в символах исходного текста, из которого был получен текущий фрагмент. Нулевое значение обозначает соответствие символов по символам между исходным текстом и производным текстом. Ненулевое значение означает, что прямая корреспонденция не существует.

*квкстартсаурце*<br/>
Смещение, с которого исходный текст для производного фрагмента начинается в исходном блоке.

*чункбреактипе*<br/>
Тип разрыва, разделяющий предыдущий фрагмент из текущего фрагмента. Значения из перечисления CHUNK_BREAKTYPE.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplsetintvalue"></a><a name="setintvalue"></a> Кмфкфилтерчунквалуеимпл:: Сетинтвалуе

Присвойте свойству по ключу значение int.

```
HRESULT SetIntValue(
    REFPROPERTYKEY pkey,
    int nVal,
    CHUNKSTATE chunkType = CHUNK_VALUE,
    LCID locale = 0,
    DWORD cwcLenSource = 0,
    DWORD cwcStartSource = 0,
    CHUNK_BREAKTYPE chunkBreakType = CHUNK_NO_BREAK);
```

### <a name="parameters"></a>Параметры

*PKEY*<br/>
Указывает ключ свойства.

*Непредвиденное nval*<br/>
Задает заданное значение фрагмента.

*чунктипе*<br/>
Флаги указывают, содержит ли этот блок тип Text-Type или свойство значения. Значения флагов берутся из перечисления ЧУНКСТАТЕ.

*locale*<br/>
Язык и подязык, связанные с фрагментом текста. Языковой стандарт блока данных используется индексаторами документов для выполнения правильного разбиения текста на слова. Если фрагмент не является ни текстовым типом, ни типом значения с типом данных VT_LPWSTR, VT_LPSTR или VT_BSTR, это поле игнорируется.

*квкленсаурце*<br/>
Длина в символах исходного текста, из которого был получен текущий фрагмент. Нулевое значение обозначает соответствие символов по символам между исходным текстом и производным текстом. Ненулевое значение означает, что прямая корреспонденция не существует.

*квкстартсаурце*<br/>
Смещение, с которого исходный текст для производного фрагмента начинается в исходном блоке.

*чункбреактипе*<br/>
Тип разрыва, разделяющий предыдущий фрагмент из текущего фрагмента. Значения из перечисления CHUNK_BREAKTYPE.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplsetlongvalue"></a><a name="setlongvalue"></a> Кмфкфилтерчунквалуеимпл:: Сетлонгвалуе

Задайте в качестве значения свойства Key значение LONG.

```
HRESULT SetLongValue(
    REFPROPERTYKEY pkey,
    long lVal,
    CHUNKSTATE chunkType = CHUNK_VALUE,
    LCID locale = 0,
    DWORD cwcLenSource = 0,
    DWORD cwcStartSource = 0,
    CHUNK_BREAKTYPE chunkBreakType = CHUNK_NO_BREAK);
```

### <a name="parameters"></a>Параметры

*PKEY*<br/>
Указывает ключ свойства.

*лвал*<br/>
Задает заданное значение фрагмента.

*чунктипе*<br/>
Флаги указывают, содержит ли этот блок тип Text-Type или свойство значения. Значения флагов берутся из перечисления ЧУНКСТАТЕ.

*locale*<br/>
Язык и подязык, связанные с фрагментом текста. Языковой стандарт блока данных используется индексаторами документов для выполнения правильного разбиения текста на слова. Если фрагмент не является ни текстовым типом, ни типом значения с типом данных VT_LPWSTR, VT_LPSTR или VT_BSTR, это поле игнорируется.

*квкленсаурце*<br/>
Длина в символах исходного текста, из которого был получен текущий фрагмент. Нулевое значение обозначает соответствие символов по символам между исходным текстом и производным текстом. Ненулевое значение означает, что прямая корреспонденция не существует.

*квкстартсаурце*<br/>
Смещение, с которого исходный текст для производного фрагмента начинается в исходном блоке.

*чункбреактипе*<br/>
Тип разрыва, разделяющий предыдущий фрагмент из текущего фрагмента. Значения из перечисления CHUNK_BREAKTYPE.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplsetsystemtimevalue"></a><a name="setsystemtimevalue"></a> Кмфкфилтерчунквалуеимпл:: Сетсистемтимевалуе

Задает свойство по ключу для SystemTime.

```
HRESULT SetSystemTimeValue(
    REFPROPERTYKEY pkey,
    const SYSTEMTIME& systemTime,
    CHUNKSTATE chunkType = CHUNK_VALUE,
    LCID locale=0,
    DWORD cwcLenSource=0,
    DWORD cwcStartSource=0,
    CHUNK_BREAKTYPE chunkBreakType=CHUNK_NO_BREAK);
```

### <a name="parameters"></a>Параметры

*PKEY*<br/>
Указывает ключ свойства.

*systemTime*<br/>
Задает заданное значение фрагмента.

*чунктипе*<br/>
Флаги указывают, содержит ли этот блок тип Text-Type или свойство значения. Значения флагов берутся из перечисления ЧУНКСТАТЕ.

*locale*<br/>
Язык и подязык, связанные с фрагментом текста. Языковой стандарт блока данных используется индексаторами документов для выполнения правильного разбиения текста на слова. Если фрагмент не является ни текстовым типом, ни типом значения с типом данных VT_LPWSTR, VT_LPSTR или VT_BSTR, это поле игнорируется.

*квкленсаурце*<br/>
Длина в символах исходного текста, из которого был получен текущий фрагмент. Нулевое значение обозначает соответствие символов по символам между исходным текстом и производным текстом. Ненулевое значение означает, что прямая корреспонденция не существует.

*квкстартсаурце*<br/>
Смещение, с которого исходный текст для производного фрагмента начинается в исходном блоке.

*чункбреактипе*<br/>
Тип разрыва, разделяющий предыдущий фрагмент из текущего фрагмента. Значения из перечисления CHUNK_BREAKTYPE.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcfilterchunkvalueimplsettextvalue"></a><a name="settextvalue"></a> Кмфкфилтерчунквалуеимпл:: Сеттекствалуе

Задает свойство по ключу для строки в Юникоде.

```
HRESULT SetTextValue(
    REFPROPERTYKEY pkey,
    LPCTSTR pszValue,
    CHUNKSTATE chunkType = CHUNK_VALUE,
    LCID locale = 0,
    DWORD cwcLenSource = 0,
    DWORD cwcStartSource = 0,
    CHUNK_BREAKTYPE chunkBreakType = CHUNK_NO_BREAK);
```

### <a name="parameters"></a>Параметры

*PKEY*<br/>
Указывает ключ свойства.

*псзвалуе*<br/>
Задает заданное значение фрагмента.

*чунктипе*<br/>
Флаги указывают, содержит ли этот блок тип Text-Type или свойство значения. Значения флагов берутся из перечисления ЧУНКСТАТЕ.

*locale*<br/>
Язык и подязык, связанные с фрагментом текста. Языковой стандарт блока данных используется индексаторами документов для выполнения правильного разбиения текста на слова. Если фрагмент не является ни текстовым типом, ни типом значения с типом данных VT_LPWSTR, VT_LPSTR или VT_BSTR, это поле игнорируется.

*квкленсаурце*<br/>
Длина в символах исходного текста, из которого был получен текущий фрагмент. Нулевое значение обозначает соответствие символов по символам между исходным текстом и производным текстом. Ненулевое значение означает, что прямая корреспонденция не существует.

*квкстартсаурце*<br/>
Смещение, с которого исходный текст для производного фрагмента начинается в исходном блоке.

*чункбреактипе*<br/>
Тип разрыва, разделяющий предыдущий фрагмент из текущего фрагмента. Значения из перечисления CHUNK_BREAKTYPE.

### <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае — код ошибки.

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
