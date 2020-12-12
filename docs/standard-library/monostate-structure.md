---
description: 'Дополнительные сведения о: нештатная структура'
title: Структура с нештатным состоянием
ms.date: 04/04/2019
f1_keywords:
- variant/std::monostate
helpviewer_keywords:
- monostate struct
ms.openlocfilehash: 93b21f399761970129a495590e0821aa911a0408
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97115161"
---
# <a name="monostate-struct"></a>Структура с нештатным состоянием

Этот класс выступает в качестве альтернативного типа для варианта, чтобы сделать тип варианта по умолчанию конструируемым.

## <a name="syntax"></a>Синтаксис

```cpp
struct monostate;

constexpr bool operator<(monostate, monostate) noexcept;
constexpr bool operator>(monostate, monostate) noexcept;
constexpr bool operator<=(monostate, monostate) noexcept;
constexpr bool operator>=(monostate, monostate) noexcept;
constexpr bool operator==(monostate, monostate) noexcept;
constexpr bool operator!=(monostate, monostate) noexcept;
```
