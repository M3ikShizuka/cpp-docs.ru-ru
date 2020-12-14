---
description: 'Дополнительные сведения о: Ошибка компилятора C2778'
title: Ошибка компилятора C2778
ms.date: 11/04/2016
f1_keywords:
- C2778
helpviewer_keywords:
- C2778
ms.assetid: b24cb732-2914-42cc-8928-e2d87b393428
ms.openlocfilehash: e614ed5ee94a4876a687bfa8257abc5bcd9d8587
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298075"
---
# <a name="compiler-error-c2778"></a>Ошибка компилятора C2778

неправильно сформированный GUID в __declspec (UUID ())

В расширенном атрибуте [UUID](../../cpp/uuid-cpp.md) указан неверный идентификатор GUID.

GUID должен быть строкой шестнадцатеричных чисел в следующем формате:

```cpp
// C2778a.cpp
// compile with: /c
struct __declspec(uuid("00000000-0000-0000-0000-000000000000")) A {};
struct __declspec(uuid("{00000000-0000-0000-0000-000000000000}")) B{};
```

`uuid`Расширенный атрибут принимает строки, распознаваемые [клсидфромстринг](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring), с разделителями фигурных скобок или без них.

Следующий пример приводит к возникновению ошибки C2778:

```cpp
// C2778b.cpp
struct __declspec(uuid(" 00000000-0000-0000-0000-000000000000 ")) C { };   // C2778
struct __declspec(uuid("00000000000000000000000000000000")) D { };   // C2778
```
