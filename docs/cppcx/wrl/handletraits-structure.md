---
description: 'Дополнительные сведения о: структура метод HandleTraits'
title: HANDLETraits - структура
ms.date: 09/27/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits::Close
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits::GetInvalidValue
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits structure
- Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits::Close method
- Microsoft::WRL::Wrappers::HandleTraits::HANDLETraits::GetInvalidValue method
ms.assetid: 22963e88-d857-4624-9182-7c986daff722
ms.openlocfilehash: c3eef03c724b1ba868ba67ed251acdb310d8b66f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97250027"
---
# <a name="handletraits-structure"></a>HANDLETraits - структура

Определяет общие характеристики дескриптора.

## <a name="syntax"></a>Синтаксис

```cpp
struct HANDLETraits;
```

## <a name="members"></a>Члены

### <a name="public-typedefs"></a>Общедоступные определения типов

Имя   | Описание
------ | ---------------------
`Type` | Синоним для HANDLE.

### <a name="public-methods"></a>Открытые методы

name                                              | Описание
------------------------------------------------- | -----------------------------
[Метод HandleTraits:: Close](#close)                     | Закрывает указанный маркер.
[Метод HandleTraits:: GetInvalidValue](#getinvalidvalue) | Представляет недопустимый Handle.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`HANDLETraits`

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Microsoft:: WRL:: оболочки:: метод HandleTraits

## <a name="handletraitsclose"></a><a name="close"></a> Метод HandleTraits:: Close

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

## <a name="handletraitsgetinvalidvalue"></a><a name="getinvalidvalue"></a> Метод HandleTraits:: GetInvalidValue

Представляет недопустимый Handle.

```cpp
inline static HANDLE GetInvalidValue();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение INVALID_HANDLE_VALUE (INVALID_HANDLE_VALUE определяется Windows).
