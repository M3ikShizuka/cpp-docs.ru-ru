---
description: 'Дополнительные сведения о: структура константа argtraitshelper'
title: ArgTraitsHelper - структура
ms.date: 09/21/2018
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::Details::ArgTraitsHelper
- event/Microsoft::WRL::Details::ArgTraitsHelper::args
helpviewer_keywords:
- Microsoft::WRL::Details::ArgTraitsHelper structure
- Microsoft::WRL::Details::ArgTraitsHelper::args constant
ms.assetid: e3f798da-0aef-4a57-95d3-d38c34c47d72
ms.openlocfilehash: a749c48c72c837eb0898d32ddd08410b87918871
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175863"
---
# <a name="argtraitshelper-structure"></a>ArgTraitsHelper - структура

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename TDelegateInterface>
struct ArgTraitsHelper;
```

### <a name="parameters"></a>Параметры

*тделегатеинтерфаце*<br/>
Интерфейс делегата.

## <a name="remarks"></a>Комментарии

Помогает определить общие характеристики аргументов делегата.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

Имя         | Описание
------------ | ------------------------------------------------------
`methodType` | Синоним для `decltype(&TDelegateInterface::Invoke)`.
`Traits`     | Синоним для `ArgTraits<methodType>`.

### <a name="public-constants"></a>Открытые константы

Имя                           | Описание
------------------------------ | ---------------------------------------------------------------------------------------------------------------------
[Константа argtraitshelper:: args](#args) | Помогает [константа ArgTraits:: args](#args) отображать число параметров в `Invoke` методе интерфейса делегата.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`ArgTraitsHelper`

## <a name="requirements"></a>Требования

**Заголовок:** Event. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="argtraitshelperargs"></a><a name="args"></a> Константа argtraitshelper:: args

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
static const int args = Traits::args;
```

### <a name="remarks"></a>Комментарии

Помогает `ArgTraitsHelper::args` синхронизировать количество параметров в `Invoke` методе интерфейса делегата.
