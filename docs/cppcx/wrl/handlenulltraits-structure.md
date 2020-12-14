---
description: 'Дополнительные сведения о: структура метод handlenulltraits'
title: HANDLENullTraits - структура
ms.date: 09/27/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLENullTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLENullTraits::Close
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLENullTraits::GetInvalidValue
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::HANDLENullTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::HANDLENullTraits::Close method
- Microsoft::WRL::Wrappers::HandleTraits::HANDLENullTraits::GetInvalidValue method
ms.assetid: 88a29a14-c516-40cb-a0ca-ee897a668623
ms.openlocfilehash: 14d5eaab36be24b5450b66c35c9cf5cbba39ea4d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97229253"
---
# <a name="handlenulltraits-structure"></a>HANDLENullTraits - структура

Определяет общие характеристики неинициализированного маркера.

## <a name="syntax"></a>Синтаксис

```cpp
struct HANDLENullTraits;
```

## <a name="members"></a>Члены

### <a name="public-typedefs"></a>Общедоступные определения типов

Имя   | Описание
------ | ---------------------
`Type` | Синоним для HANDLE.

### <a name="public-methods"></a>Открытые методы

name                                                  | Описание
----------------------------------------------------- | -----------------------------
[Метод handlenulltraits:: Close](#close)                     | Закрывает указанный маркер.
[Метод handlenulltraits:: GetInvalidValue](#getinvalidvalue) | Представляет недопустимый Handle.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`HANDLENullTraits`

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Microsoft:: WRL:: оболочки:: метод HandleTraits

## <a name="handlenulltraitsclose"></a><a name="close"></a> Метод handlenulltraits:: Close

Закрывает указанный маркер.

```cpp
inline static bool Close(
   _In_ Type h
);
```

### <a name="parameters"></a>Параметры

*h*<br/>
Закрывающий маркер.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если Handles *h* успешно закрыто. в противном случае — **`false`** .

## <a name="handlenulltraitsgetinvalidvalue"></a><a name="getinvalidvalue"></a> Метод handlenulltraits:: GetInvalidValue

Представляет недопустимый Handle.

```cpp
inline static Type GetInvalidValue();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает **`nullptr`** .
