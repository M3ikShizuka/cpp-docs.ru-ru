---
description: 'Дополнительные сведения о: SafeIntException Class'
title: Класс SafeIntException
ms.date: 10/22/2018
ms.topic: reference
f1_keywords:
- SafeIntException Class
- SafeIntException
- SafeIntException.SafeIntException
- SafeIntException::SafeIntException
helpviewer_keywords:
- SafeIntException class
- SafeIntException, constructor
ms.assetid: 88bef958-1f48-4d55-ad4f-d1f9581a293a
ms.openlocfilehash: 6a7be21b0dfa42a23ba60eac7eb3f4ebbf1629ef
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97149582"
---
# <a name="safeintexception-class"></a>Класс SafeIntException

Класс `SafeInt` использует `SafeIntException` для определения причины, по которой не удается выполнить математическую операцию.

> [!NOTE]
> Последняя версия этой библиотеки находится по адресу [https://github.com/dcleblanc/SafeInt](https://github.com/dcleblanc/SafeInt) .

## <a name="syntax"></a>Синтаксис

```cpp
class SafeIntException;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

name                                                    | Описание
------------------------------------------------------- | ------------------------------------
[SafeIntException:: SafeIntException](#safeintexception) | Создает объект `SafeIntException`.

## <a name="remarks"></a>Комментарии

[Класс SafeInt](safeint-class.md) является единственным классом, который использует класс `SafeIntException`.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`SafeIntException`

## <a name="requirements"></a>Требования

**Заголовок:** safeint.h

**Пространство имен:** msl::utilities

## <a name="safeintexceptionsafeintexception"></a><a name="safeintexception"></a> SafeIntException:: SafeIntException

Создает объект `SafeIntException`.

```cpp
SafeIntException();

SafeIntException(
   SafeIntError code
);
```

### <a name="parameters"></a>Параметры

*code*<br/>
[in] Значение перечислимых данных, описывающее возникшую ошибку.

### <a name="remarks"></a>Комментарии

Возможные значения для параметра *code* определены в файле Safeint.h. Для удобства эти возможные значения также перечислены здесь.

- `SafeIntNoError`
- `SafeIntArithmeticOverflow`
- `SafeIntDivideByZero`
