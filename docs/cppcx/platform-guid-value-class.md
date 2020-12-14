---
description: 'Дополнительные сведения: класс значений Platform:: GUID'
title: Класс значения Platform::Guid
ms.date: 01/15/2019
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Guid
helpviewer_keywords:
- Platform::Guid Struct
ms.assetid: 25c0bfb2-7f93-44d8-bdf4-ef4fbac3424a
ms.openlocfilehash: 4c2ffc5096e6b40266fef0934acc562edf721c24
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97195194"
---
# <a name="platformguid-value-class"></a>Класс значения Platform::Guid

Представляет [GUID] (тип/Windows/Win32/API/guiddef/NS-guiddef-GUID в системе типов среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
public value struct Guid
```

### <a name="members"></a>Члены

`Platform::Guid` содержит `Equals()` методы, `GetHashCode()` и, `ToString()` производные от [класса Platform:: Object](../cppcx/platform-object-class.md), и метод, `GetTypeCode()` производный от [класса Platform:: Type](../cppcx/platform-type-class.md). `Platform::Guid` также содержит следующие члены.

|Член|Описание|
|------------|-----------------|
|[Устройства](#ctor)|Инициализирует новый экземпляр `Platform::Guid`.|
|[Оператор = =](#operator-equality)|Оператор «равно».|
|[operator! =](#operator-inequality)|Оператор «не равно».|
|[станции&lt;](#operator-less)|Оператор «меньше».|
|[оператор ()](#operator-call)|Преобразует `Platform::Guid` в `GUID`.|

### <a name="remarks"></a>Комментарии

Чтобы создать новый объект `Platform::Guid` , используйте статический метод [Windows:: Foundation:: GuidHelper:: креатеневгуид](/uwp/api/windows.foundation.guidhelper.createnewguid) .

### <a name="requirements"></a>Требования

**Минимальный поддерживаемый клиент:** Windows 8

**Минимальный поддерживаемый сервер:** Windows Server 2012

**Пространство имен:** Platform

**Метаданные:** Platform. winmd

## <a name="guidguid-constructors"></a><a name="ctor"></a> Конструкторы GUID:: GUID

Инициализирует новый экземпляр `Platform::Guid`.

### <a name="syntax"></a>Синтаксис

```cpp
Guid(
    unsigned int a,
    unsigned short b,
    unsigned short c,
    unsigned char d,
    unsigned char e,
    unsigned char f,
    unsigned char g,
    unsigned char h,
    unsigned char i,
    unsigned char j,
    unsigned char k );

Guid(GUID m);

Guid(
    unsigned int a,
    unsigned short b,
    unsigned short c,
    Array<unsigned char>^ n );
```

### <a name="parameters"></a>Параметры

*конкретного*<br/>
Первые 4 байта объекта `GUID` .

*b*<br/>
Следующие 2 байта `GUID` .

*c*<br/>
Следующие 2 байта `GUID` .

*d*<br/>
Следующий байт структуры `GUID`.

*e*<br/>
Следующий байт структуры `GUID`.

*f*<br/>
Следующий байт структуры `GUID`.

*g*<br/>
Следующий байт структуры `GUID`.

*h*<br/>
Следующий байт структуры `GUID`.

*i*<br/>
Следующий байт структуры `GUID`.

*б*<br/>
Следующий байт структуры `GUID`.

*занят*<br/>
Следующий байт структуры `GUID`.

*m*<br/>
A `GUID` в виде [структуры GUID](/windows/win32/api/guiddef/ns-guiddef-guid).

*n*<br/>
Оставшиеся 8 байт объекта `GUID` .

## <a name="guidoperator-operator"></a><a name="operator-equality"></a> Оператор GUID:: operator = =

Сравнивает два экземпляра `Platform::Guid` на предмет их равенства.

### <a name="syntax"></a>Синтаксис

```cpp
static bool Platform::Guid::operator==(Platform::Guid guid1, Platform::Guid guid2);
```

### <a name="parameters"></a>Параметры

*GUID1*<br/>
Первый экземпляр `Platform::Guid` для сравнения.

*GUID2*<br/>
Второй экземпляр `Platform::Guid` для сравнения.

### <a name="return-value"></a>Возвращаемое значение

Значение true, если два `Platform::Guid` экземпляра равны.

### <a name="remarks"></a>Комментарии

Предпочитать использование `==` оператора вместо статического метода [Windows:: Foundation:: GuidHelper:: Equals](/uwp/api/windows.foundation.guidhelper.equals) .

## <a name="guidoperator-operator"></a><a name="operator-inequality"></a> Оператор GUID:: operator! =

Сравнивает два экземпляра `Platform::Guid` на неравенство.

### <a name="syntax"></a>Синтаксис

```cpp
static bool Platform::Guid::operator!=(Platform::Guid guid1, Platform::Guid guid2);
```

### <a name="parameters"></a>Параметры

*GUID1*<br/>
Первый экземпляр `Platform::Guid` для сравнения.

*GUID2*<br/>
Второй экземпляр `Platform::Guid` для сравнения.

### <a name="return-value"></a>Возвращаемое значение

Значение true, если два `Platform::Guid` экземпляра не равны.

## <a name="guidoperatorlt-operator"></a><a name="operator-less"></a>Оператор GUID:: operator &lt;

Сравнивает два `Platform::Guid` экземпляра для упорядочения.

### <a name="syntax"></a>Синтаксис

```cpp
static bool Platform::Guid::operator<(Platform::Guid guid1, Platform::Guid guid2);
```

### <a name="parameters"></a>Параметры

*GUID1*<br/>
Первый экземпляр `Platform::Guid` для сравнения.

*GUID2*<br/>
Второй экземпляр `Platform::Guid` для сравнения.

### <a name="return-value"></a>Возвращаемое значение

Значение true, если *GUID1* упорядочивается до *GUID2*. Упорядочение лексикографическим порядком после обработки каждого `Platform::Guid` , как если бы он был массивом из 4 32-разрядных беззнаковых значений. Это не порядок, используемый SQL Server или .NET Framework, а также не совпадает с лексикографическом упорядочиванием по строковому представлению.

Этот оператор предоставляется таким образом, чтобы `Guid` объекты могли проще использовать стандартную библиотеку C++.

## <a name="guidoperator-operator"></a><a name="operator-call"></a> Оператор GUID:: operator ()

Неявно преобразует в `Platform::Guid` [структуру GUID](/windows/win32/api/guiddef/ns-guiddef-guid).

### <a name="syntax"></a>Синтаксис

```cpp
const GUID& Platform::Guid::operator();
```

### <a name="return-value"></a>Возвращаемое значение

[Структура Guid](/windows/win32/api/guiddef/ns-guiddef-guid).

## <a name="see-also"></a>См. также раздел

[Пространство имен Platform](../cppcx/platform-namespace-c-cx.md)
