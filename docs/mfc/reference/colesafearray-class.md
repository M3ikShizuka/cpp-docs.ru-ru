---
description: 'Дополнительные сведения о: Колесафеаррай Class'
title: Класс Колесафеаррай
ms.date: 08/29/2019
f1_keywords:
- COleSafeArray
- AFXDISP/COleSafeArray
- AFXDISP/COleSafeArray::COleSafeArray
- AFXDISP/COleSafeArray::AccessData
- AFXDISP/COleSafeArray::AllocData
- AFXDISP/COleSafeArray::AllocDescriptor
- AFXDISP/COleSafeArray::Attach
- AFXDISP/COleSafeArray::Clear
- AFXDISP/COleSafeArray::Copy
- AFXDISP/COleSafeArray::Create
- AFXDISP/COleSafeArray::CreateOneDim
- AFXDISP/COleSafeArray::Destroy
- AFXDISP/COleSafeArray::DestroyData
- AFXDISP/COleSafeArray::DestroyDescriptor
- AFXDISP/COleSafeArray::Detach
- AFXDISP/COleSafeArray::GetByteArray
- AFXDISP/COleSafeArray::GetDim
- AFXDISP/COleSafeArray::GetElement
- AFXDISP/COleSafeArray::GetElemSize
- AFXDISP/COleSafeArray::GetLBound
- AFXDISP/COleSafeArray::GetOneDimSize
- AFXDISP/COleSafeArray::GetUBound
- AFXDISP/COleSafeArray::Lock
- AFXDISP/COleSafeArray::PtrOfIndex
- AFXDISP/COleSafeArray::PutElement
- AFXDISP/COleSafeArray::Redim
- AFXDISP/COleSafeArray::ResizeOneDim
- AFXDISP/COleSafeArray::UnaccessData
- AFXDISP/COleSafeArray::Unlock
helpviewer_keywords:
- COleSafeArray [MFC], COleSafeArray
- COleSafeArray [MFC], AccessData
- COleSafeArray [MFC], AllocData
- COleSafeArray [MFC], AllocDescriptor
- COleSafeArray [MFC], Attach
- COleSafeArray [MFC], Clear
- COleSafeArray [MFC], Copy
- COleSafeArray [MFC], Create
- COleSafeArray [MFC], CreateOneDim
- COleSafeArray [MFC], Destroy
- COleSafeArray [MFC], DestroyData
- COleSafeArray [MFC], DestroyDescriptor
- COleSafeArray [MFC], Detach
- COleSafeArray [MFC], GetByteArray
- COleSafeArray [MFC], GetDim
- COleSafeArray [MFC], GetElement
- COleSafeArray [MFC], GetElemSize
- COleSafeArray [MFC], GetLBound
- COleSafeArray [MFC], GetOneDimSize
- COleSafeArray [MFC], GetUBound
- COleSafeArray [MFC], Lock
- COleSafeArray [MFC], PtrOfIndex
- COleSafeArray [MFC], PutElement
- COleSafeArray [MFC], Redim
- COleSafeArray [MFC], ResizeOneDim
- COleSafeArray [MFC], UnaccessData
- COleSafeArray [MFC], Unlock
ms.assetid: f45a5224-5f48-40ec-9ddd-287ef9740150
ms.openlocfilehash: 6c33f58f71167c492883a25b05fce6bb8fb09916
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226705"
---
# <a name="colesafearray-class"></a>Класс Колесафеаррай

Класс для работы с массивами произвольных типов и измерений.

## <a name="syntax"></a>Синтаксис

```
class COleSafeArray : public tagVARIANT
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Колесафеаррай:: Колесафеаррай](#colesafearray)|Формирует объект `COleSafeArray`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Колесафеаррай:: Акцессдата](#accessdata)|Извлекает указатель на данные массива.|
|[Колесафеаррай:: Аллокдата](#allocdata)|Выделяет память для массива.|
|[Колесафеаррай:: Аллокдескриптор](#allocdescriptor)|Выделяет память для дескриптора безопасного массива.|
|[Колесафеаррай:: Attach](#attach)|Предоставляет Управление существующим `VARIANT` массивом `COleSafeArray` объекту.|
|[Колесафеаррай:: Clear](#clear)|Освобождает все данные в базовом `VARIANT` .|
|[Колесафеаррай:: Copy](#copy)|Создает копию существующего массива.|
|[Колесафеаррай:: Create](#create)|Создает надежный массив.|
|[Колесафеаррай:: Креатеонедим](#createonedim)|Создает одномерный `COleSafeArray` объект.|
|[Колесафеаррай::D естрой](#destroy)|Уничтожает существующий массив.|
|[Колесафеаррай::D Естройдата](#destroydata)|Уничтожает данные в надежном массиве.|
|[Колесафеаррай::D Естройдескриптор](#destroydescriptor)|Уничтожает дескриптор безопасного массива.|
|[Колесафеаррай::D етач](#detach)|Отсоединяет массив вариантов от `COleSafeArray` объекта (так что данные не будут освобождены).|
|[Колесафеаррай:: Жетбитеаррай](#getbytearray)|Копирует содержимое безопасного массива в [CByteArray](../../mfc/reference/cbytearray-class.md).|
|[Колесафеаррай:: Жетдим](#getdim)|Возвращает число измерений в массиве.|
|[Колесафеаррай:: элемент](#getelement)|Извлекает один элемент безопасного массива.|
|[Колесафеаррай:: Жетелемсизе](#getelemsize)|Возвращает размер одного элемента в массиве безопасного массива (в байтах).|
|[Колесафеаррай:: Жетлбаунд](#getlbound)|Возвращает нижнюю границу любого измерения безопасного массива.|
|[Колесафеаррай:: Жетонедимсизе](#getonedimsize)|Возвращает количество элементов в одномерном `COleSafeArray` объекте.|
|[Колесафеаррай:: Жетубаунд](#getubound)|Возвращает верхнюю границу любого измерения безопасного массива.|
|[Колесафеаррай:: Lock](#lock)|Увеличивает счетчик блокировок массива и помещает указатель на данные массива в дескрипторе массива.|
|[Колесафеаррай::P Трофиндекс](#ptrofindex)|Возвращает указатель на индексированный элемент.|
|[Колесафеаррай::P Утелемент](#putelement)|Помещает в массив один элемент.|
|[Колесафеаррай:: ReDim](#redim)|Изменяет наименее значимую (правую) границу безопасного массива.|
|[Колесафеаррай:: Ресизеонедим](#resizeonedim)|Изменяет число элементов в одномерном `COleSafeArray` объекте.|
|[Колесафеаррай:: Унакцессдата](#unaccessdata)|Уменьшает счетчик блокировок массива и делает недействительным указатель, извлеченный `AccessData` .|
|[Колесафеаррай:: Unlock](#unlock)|Уменьшает счетчик блокировок массива, чтобы его можно было освободить или изменить его размер.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Колесафеаррай:: operator ЛПКВАРИАНТ](#operator_lpcvariant)|Обращается к базовой `VARIANT` структуре `COleSafeArray` объекта.|
|[Колесафеаррай:: operator ЛПВАРИАНТ](#operator_lpvariant)|Обращается к базовой `VARIANT` структуре `COleSafeArray` объекта.|
|[Колесафеаррай:: operator =](#operator_eq)|Копирует значения в `COleSafeArray` объект ( `SAFEARRAY` ,, `VARIANT` `COleVariant` или `COleSafeArray` массив).|
|[Колесафеаррай:: operator = =](#operator_eq_eq)|Сравнивает два вариативных массива ( `SAFEARRAY` ,, `VARIANT` `COleVariant` или `COleSafeArray` ).|
|[Колесафеаррай:: operator &lt;&lt;](#operator_lt_lt)|Выводит содержимое `COleSafeArray` объекта в контекст дампа.|

## <a name="remarks"></a>Комментарии

`COleSafeArray` является производным от `VARIANT` структуры OLE. Функции- `SAFEARRAY` члены OLE доступны через `COleSafeArray` , а также набор функций-членов, специально разработанных для одномерные массивов байтов.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`tagVARIANT`

`COleSafeArray`

## <a name="requirements"></a>Требования

**Заголовок:** afxdisp.h

## <a name="colesafearrayaccessdata"></a><a name="accessdata"></a> Колесафеаррай:: Акцессдата

Извлекает указатель на данные массива.

```cpp
void AccessData(void** ppvData);
```

### <a name="parameters"></a>Параметры

*ппвдата*<br/>
Указатель на указатель на данные массива.

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCOleContainer#26](../../mfc/codesnippet/cpp/colesafearray-class_1.cpp)]

## <a name="colesafearrayallocdata"></a><a name="allocdata"></a> Колесафеаррай:: Аллокдата

Выделяет память для безопасного массива.

```cpp
void AllocData();
```

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

## <a name="colesafearrayallocdescriptor"></a><a name="allocdescriptor"></a> Колесафеаррай:: Аллокдескриптор

Выделяет память для дескриптора безопасного массива.

```cpp
void AllocDescriptor(DWORD dwDims);
```

### <a name="parameters"></a>Параметры

*двдимс*<br/>
Число измерений в надежном массиве.

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

## <a name="colesafearrayattach"></a><a name="attach"></a> Колесафеаррай:: Attach

Предоставляет управление данными в существующем `VARIANT` массиве `COleSafeArray` объекту.

```cpp
void Attach(VARIANT& varSrc);
```

### <a name="parameters"></a>Параметры

*varSrc*<br/>
Объект `VARIANT`. Параметр *варсрк* должен иметь значение VarType [VT_ARRAY](/windows/win32/api/wtypes/ne-wtypes-varenum).

### <a name="remarks"></a>Комментарии

`VARIANT`Для типа источника задано значение VT_EMPTY. Эта функция очищает текущие данные массива, если таковые имеются.

### <a name="example"></a>Пример

  См. пример для [колесафеаррай:: акцессдата](#accessdata).

## <a name="colesafearrayclear"></a><a name="clear"></a> Колесафеаррай:: Clear

Очищает защищенный массив.

```cpp
void Clear();
```

### <a name="remarks"></a>Комментарии

Функция очищает защищенный массив, устанавливая `VARTYPE` для объекта значение VT_EMPTY. Текущее содержимое освобождается, а массив освобождается.

## <a name="colesafearraycolesafearray"></a><a name="colesafearray"></a> Колесафеаррай:: Колесафеаррай

Формирует объект `COleSafeArray`.

```
COleSafeArray();

COleSafeArray(
    const SAFEARRAY& saSrc,
    VARTYPE vtSrc);

COleSafeArray(
    LPCSAFEARRAY pSrc,
    VARTYPE vtSrc);

COleSafeArray(const COleSafeArray& saSrc);
COleSafeArray(const VARIANT& varSrc);
COleSafeArray(LPCVARIANT pSrc);
COleSafeArray(const COleVariant& varSrc);
```

### <a name="parameters"></a>Параметры

*сасрк*<br/>
Существующий `COleSafeArray` объект или `SAFEARRAY` для копирования в новый `COleSafeArray` объект.

*втсрк*<br/>
Объект VARTYPE нового `COleSafeArray` объекта.

*псасрк*<br/>
Указатель на объект, `SAFEARRAY` который необходимо скопировать в новый `COleSafeArray` объект.

*varSrc*<br/>
Существующий `VARIANT` объект или `COleVariant` , который будет скопирован в новый `COleSafeArray` объект.

*pSrc*<br/>
Указатель на `VARIANT` объект, который необходимо скопировать в новый `COleSafeArray` объект.

### <a name="remarks"></a>Комментарии

Все эти конструкторы создают новые `COleSafeArray` объекты. Если параметр отсутствует, `COleSafeArray` создается пустой объект (VT_EMPTY). Если `COleSafeArray` копируется из другого массива, для которого определено неявное значение VarType (a `COleSafeArray` , `COleVariant` или `VARIANT` ), то VarType исходного массива сохраняется, и его не нужно указывать. Если `COleSafeArray` копируется из другого массива, у которого нет известного параметра VarType ( `SAFEARRAY` ), необходимо указать VarType в параметре *втсрк* .

При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

## <a name="colesafearraycopy"></a><a name="copy"></a> Колесафеаррай:: Copy

Создает копию существующего безопасного массива.

```cpp
void Copy(LPSAFEARRAY* ppsa);
```

### <a name="parameters"></a>Параметры

*ппса*<br/>
Указатель на расположение, в котором возвращается новый дескриптор массива.

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

## <a name="colesafearraycreate"></a><a name="create"></a> Колесафеаррай:: Create

Выделяет и инициализирует данные для массива.

```cpp
void Create(
    VARTYPE vtSrc,
    DWORD dwDims,
    DWORD* rgElements);

void Create(
    VARTYPE vtSrc,
    DWORD dwDims,
    SAFEARRAYBOUND* rgsabounds);
```

### <a name="parameters"></a>Параметры

*втсрк*<br/>
Базовый тип массива (то есть VARTYPE каждого элемента массива). Переменная VARTYPE ограничена подмножеством типов Variant. Не может быть задан ни VT_ARRAY, ни флаг VT_BYREF. VT_EMPTY и VT_NULL не являются допустимыми базовыми типами для массива. Все остальные типы являются допустимыми.

*двдимс*<br/>
Число измерений в массиве. Его можно изменить после создания массива с помощью [ReDim](#redim).

*ржелементс*<br/>
Указатель на массив числа элементов для каждого измерения в массиве.

*ргсабаундс*<br/>
Указатель на вектор границ (по одному для каждого измерения), выделяемый для массива.

### <a name="remarks"></a>Комментарии

Эта функция при необходимости очистит текущие данные массива. При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCOleContainer#27](../../mfc/codesnippet/cpp/colesafearray-class_2.cpp)]

## <a name="colesafearraycreateonedim"></a><a name="createonedim"></a> Колесафеаррай:: Креатеонедим

Создает новый одномерный `COleSafeArray` объект.

```cpp
void CreateOneDim(
    VARTYPE vtSrc,
    DWORD dwElements,
    const void* pvSrcData = NULL,
    long nLBound = 0);
```

### <a name="parameters"></a>Параметры

*втсрк*<br/>
Базовый тип массива (то есть VARTYPE каждого элемента массива).

*двелементс*<br/>
Число элементов в массиве. Его можно изменить после создания массива с помощью [ресизеонедим](#resizeonedim).

*пвсркдата*<br/>
Указатель на данные, копируемые в массив.

*нлбаунд*<br/>
Нижняя граница массива.

### <a name="remarks"></a>Комментарии

Функция выделяет и инициализирует данные для массива, копируя указанные данные, если указатель *пвсркдата* не равен null.

При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCOleContainer#28](../../mfc/codesnippet/cpp/colesafearray-class_3.cpp)]

## <a name="colesafearraydestroy"></a><a name="destroy"></a> Колесафеаррай::D естрой

Уничтожает существующий дескриптор массива и все данные в массиве.

```cpp
void Destroy();
```

### <a name="remarks"></a>Комментарии

Если объекты хранятся в массиве, каждый объект освобождается. При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

## <a name="colesafearraydestroydata"></a><a name="destroydata"></a> Колесафеаррай::D Естройдата

Уничтожает все данные в надежном массиве.

```cpp
void DestroyData();
```

### <a name="remarks"></a>Комментарии

Если объекты хранятся в массиве, каждый объект освобождается. При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

## <a name="colesafearraydestroydescriptor"></a><a name="destroydescriptor"></a> Колесафеаррай::D Естройдескриптор

Уничтожает дескриптор безопасного массива.

```cpp
void DestroyDescriptor();
```

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

## <a name="colesafearraydetach"></a><a name="detach"></a> Колесафеаррай::D етач

Отсоединяет `VARIANT` данные от `COleSafeArray` объекта.

```
VARIANT Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Базовое `VARIANT` значение в `COleSafeArray` объекте.

### <a name="remarks"></a>Комментарии

Функция отсоединяет данные в надежном массиве, устанавливая VARTYPE объекта в значение VT_EMPTY. Ответственность за освобождение массива путем вызова функции Windows [вариантклеар](/windows/win32/api/oleauto/nf-oleauto-variantclear).

При возникновении ошибки функция создает исключение [COleException](../../mfc/reference/coleexception-class.md).

### <a name="example"></a>Пример

  См. пример для [колесафеаррай::P утелемент](#putelement).

## <a name="colesafearraygetbytearray"></a><a name="getbytearray"></a> Колесафеаррай:: Жетбитеаррай

Копирует содержимое безопасного массива в `CByteArray` .

```cpp
void GetByteArray(CByteArray& bytes);
```

### <a name="parameters"></a>Параметры

*bytes*<br/>
Ссылка на объект [CByteArray](../../mfc/reference/cbytearray-class.md) .

## <a name="colesafearraygetdim"></a><a name="getdim"></a> Колесафеаррай:: Жетдим

Возвращает количество измерений в `COleSafeArray` объекте.

```
DWORD GetDim();
```

### <a name="return-value"></a>Возвращаемое значение

Число измерений в надежном массиве.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCOleContainer#27](../../mfc/codesnippet/cpp/colesafearray-class_2.cpp)]

## <a name="colesafearraygetelement"></a><a name="getelement"></a> Колесафеаррай:: элемент

Извлекает один элемент безопасного массива.

```cpp
void GetElement(
    long* rgIndices,
    void* pvData);
```

### <a name="parameters"></a>Параметры

*ргиндицес*<br/>
Указатель на массив индексов для каждого измерения массива.

*пвдата*<br/>
Указатель на расположение для размещения элемента массива.

### <a name="remarks"></a>Комментарии

Эта функция автоматически вызывает функции Windows `SafeArrayLock` и `SafeArrayUnlock` до и после получения элемента. Если элемент Data является строкой, объектом или вариантом, функция копирует элемент правильным образом. Параметр *пвдата* должен указывать на большой размер буфера, чтобы вместить элемент.

При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCOleContainer#29](../../mfc/codesnippet/cpp/colesafearray-class_4.cpp)]

## <a name="colesafearraygetelemsize"></a><a name="getelemsize"></a> Колесафеаррай:: Жетелемсизе

Возвращает размер элемента в `COleSafeArray` объекте.

```
DWORD GetElemSize();
```

### <a name="return-value"></a>Возвращаемое значение

Размер (в байтах) элементов безопасного массива.

## <a name="colesafearraygetlbound"></a><a name="getlbound"></a> Колесафеаррай:: Жетлбаунд

Возвращает нижнюю границу для любого измерения `COleSafeArray` объекта.

```cpp
void GetLBound(
    DWORD dwDim,
    long* pLBound);
```

### <a name="parameters"></a>Параметры

*двдим*<br/>
Измерение массива, для которого необходимо получить нижнюю границу.

*плбаунд*<br/>
Указатель на расположение для возврата нижней границы.

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [COleException](../../mfc/reference/coleexception-class.md).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCOleContainer#30](../../mfc/codesnippet/cpp/colesafearray-class_5.cpp)]

## <a name="colesafearraygetonedimsize"></a><a name="getonedimsize"></a> Колесафеаррай:: Жетонедимсизе

Возвращает количество элементов в одномерном `COleSafeArray` объекте.

```
DWORD GetOneDimSize();
```

### <a name="return-value"></a>Возвращаемое значение

Число элементов одномерного безопасного массива.

### <a name="example"></a>Пример

  См. пример для [колесафеаррай:: креатеонедим](#createonedim).

## <a name="colesafearraygetubound"></a><a name="getubound"></a> Колесафеаррай:: Жетубаунд

Возвращает верхнюю границу любого измерения безопасного массива.

```cpp
void GetUBound(
    DWORD dwDim,
    long* pUBound);
```

### <a name="parameters"></a>Параметры

*двдим*<br/>
Измерение массива, для которого необходимо получить верхнюю границу.

*пубаунд*<br/>
Указатель на расположение для возврата верхней границы.

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [COleException](../../mfc/reference/coleexception-class.md).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCOleContainer#31](../../mfc/codesnippet/cpp/colesafearray-class_6.cpp)]

## <a name="colesafearraylock"></a><a name="lock"></a> Колесафеаррай:: Lock

Увеличивает счетчик блокировок массива и помещает указатель на данные массива в дескрипторе массива.

```cpp
void Lock();
```

### <a name="remarks"></a>Комментарии

При возникновении ошибки возникает исключение [COleException](../../mfc/reference/coleexception-class.md).

Указатель в дескрипторе массива является допустимым до `Unlock` вызова метода. Вызовы `Lock` могут быть вложенными; требуется равное число вызовов `Unlock` .

Невозможно удалить массив, пока он заблокирован.

## <a name="colesafearrayoperator-lpcvariant"></a><a name="operator_lpcvariant"></a> Колесафеаррай:: operator ЛПКВАРИАНТ

Вызовите этот оператор приведения, чтобы получить доступ к базовой `VARIANT` структуре для этого `COleSafeArray` объекта.

```
operator LPCVARIANT() const;
```

## <a name="colesafearrayoperator-lpvariant"></a><a name="operator_lpvariant"></a> Колесафеаррай:: operator ЛПВАРИАНТ

Вызовите этот оператор приведения, чтобы получить доступ к базовой `VARIANT` структуре для этого `COleSafeArray` объекта.

```
operator LPVARIANT();
```

### <a name="remarks"></a>Комментарии

Обратите внимание, что изменение значения в `VARIANT` структуре, к которой обращается указатель, возвращаемой этой функцией, приведет к изменению значения этого `COleSafeArray` объекта.

## <a name="colesafearrayoperator-"></a><a name="operator_eq"></a> Колесафеаррай:: operator =

Эти перегруженные операторы присваивания копируют исходное значение в этот `COleSafeArray` объект.

```
COleSafeArray& operator=(const COleSafeArray& saSrc);
COleSafeArray& operator=(const VARIANT& varSrc);
COleSafeArray& operator=(LPCVARIANT pSrc);
COleSafeArray& operator=(const COleVariant& varSrc);
```

### <a name="remarks"></a>Комментарии

Краткое описание каждого оператора приведено ниже.

- **operator = (** *сасрк* **)** Копирует существующий `COleSafeArray` объект в этот объект.

- **operator = (** *варсрк* **)** Копирует существующий `VARIANT` массив или `COleVariant` в этот объект.

- **operator = (** *pSrc* **)** Копирует `VARIANT` объект массива, к которому обращается *pSrc* , в этот объект.

## <a name="colesafearrayoperator-"></a><a name="operator_eq_eq"></a> Колесафеаррай:: operator = =

Этот оператор сравнивает два массива ( `SAFEARRAY` `VARIANT` `COleVariant` массивы,, или `COleSafeArray` ) и возвращает ненулевое значение, если они равны; в противном случае — 0.

```
BOOL operator==(const SAFEARRAY& saSrc) const;  BOOL operator==(LPCSAFEARRAY pSrc) const;

BOOL operator==(const COleSafeArray& saSrc) const;  BOOL operator==(const VARIANT& varSrc) const;

BOOL operator==(LPCVARIANT pSrc) const;  BOOL operator==(const COleVariant& varSrc) const;
```

### <a name="remarks"></a>Комментарии

Два массива равны, если они имеют одинаковое число измерений, равный размер в каждом измерении и равны значениям элементов.

## <a name="colesafearrayoperator-ltlt"></a><a name="operator_lt_lt"></a> Колесафеаррай:: operator &lt;&lt;

`COleSafeArray`Оператор вставки (<<) поддерживает дамп и сохранение `COleSafeArray` объекта в архив.

```
CDumpContext& AFXAPI operator<<(
    CDumpContext& dc,
    COleSafeArray& saSrc);
```

## <a name="colesafearrayptrofindex"></a><a name="ptrofindex"></a> Колесафеаррай::P Трофиндекс

Возвращает указатель на элемент, указанный в значениях индекса.

```cpp
void PtrOfIndex(
    long* rgIndices,
    void** ppvData);
```

### <a name="parameters"></a>Параметры

*ргиндицес*<br/>
Массив значений индекса, который определяет элемент массива. Необходимо указать все индексы для элемента.

*ппвдата*<br/>
При возвращении — указатель на элемент, определяемый значениями в *ргиндицес*.

## <a name="colesafearrayputelement"></a><a name="putelement"></a> Колесафеаррай::P Утелемент

Помещает в массив один элемент.

```cpp
void PutElement(
    long* rgIndices,
    void* pvData);
```

### <a name="parameters"></a>Параметры

*ргиндицес*<br/>
Указатель на массив индексов для каждого измерения массива.

*пвдата*<br/>
Указатель на данные, которые требуется поместить в массив. Типы Variant VT_DISPATCH, VT_UNKNOWN и VT_BSTR являются указателями и не нуждаются в другом уровне косвенного обращения.

### <a name="remarks"></a>Комментарии

Эта функция автоматически вызывает функции Windows [сафеаррайлокк](/windows/win32/api/oleauto/nf-oleauto-safearraylock) и [сафеаррайунлокк](/windows/win32/api/oleauto/nf-oleauto-safearrayunlock) до и после назначения элемента. Если строка, объект или вариант являются элементом данных, функция выполняет правильное копирование, а если существующим элементом — правильное удаление.

Обратите внимание, для массива можно настроить несколько блокировок, поэтому вы можете поместить в него элементы, недоступные для других операций.

При возникновении ошибки функция создает исключение [CMemoryException](../../mfc/reference/cmemoryexception-class.md) или [COleException](../../mfc/reference/coleexception-class.md).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCOleContainer#32](../../mfc/codesnippet/cpp/colesafearray-class_7.cpp)]

## <a name="colesafearrayredim"></a><a name="redim"></a> Колесафеаррай:: ReDim

Изменяет наименее значимую (правую) границу безопасного массива.

```cpp
void Redim(SAFEARRAYBOUND* psaboundNew);
```

### <a name="parameters"></a>Параметры

*псабаунднев*<br/>
Указатель на новую структуру с привязкой к защищенному массиву, содержащую новый привязанный массив. Можно изменить только наименее значимое измерение массива.

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [COleException](../../mfc/reference/coleexception-class.md).

## <a name="colesafearrayresizeonedim"></a><a name="resizeonedim"></a> Колесафеаррай:: Ресизеонедим

Изменяет число элементов в одномерном `COleSafeArray` объекте.

```cpp
void ResizeOneDim(DWORD dwElements);
```

### <a name="parameters"></a>Параметры

*двелементс*<br/>
Количество элементов одномерного безопасного массива.

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [COleException](../../mfc/reference/coleexception-class.md).

### <a name="example"></a>Пример

  См. пример для [колесафеаррай:: креатеонедим](#createonedim).

## <a name="colesafearrayunaccessdata"></a><a name="unaccessdata"></a> Колесафеаррай:: Унакцессдата

Уменьшает счетчик блокировок массива и делает недействительным указатель, извлеченный `AccessData` .

```cpp
void UnaccessData();
```

### <a name="remarks"></a>Комментарии

При возникновении ошибки функция создает исключение [COleException](../../mfc/reference/coleexception-class.md).

### <a name="example"></a>Пример

  См. пример для [колесафеаррай:: акцессдата](#accessdata).

## <a name="colesafearrayunlock"></a><a name="unlock"></a> Колесафеаррай:: Unlock

Уменьшает счетчик блокировок массива, чтобы его можно было освободить или изменить его размер.

```cpp
void Unlock();
```

### <a name="remarks"></a>Комментарии

Эта функция вызывается после завершения доступа к данным в массиве. При возникновении ошибки возникает исключение [COleException](../../mfc/reference/coleexception-class.md).

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс COleVariant](../../mfc/reference/colevariant-class.md)<br/>
[Класс CRecordset](../../mfc/reference/crecordset-class.md)<br/>
[Класс CDatabase](../../mfc/reference/cdatabase-class.md)<br/>
