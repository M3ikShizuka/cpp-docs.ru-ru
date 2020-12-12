---
description: 'Дополнительные сведения о: Ошибка компилятора C2906'
title: Ошибка компилятора C2906
ms.date: 11/04/2016
f1_keywords:
- C2906
helpviewer_keywords:
- C2906
ms.assetid: 30f652f1-6af6-4a2f-a69e-a1a4876cc8c6
ms.openlocfilehash: 49a7e5736c1f5e1869b04e79f1c979c3620b58ed
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97270671"
---
# <a name="compiler-error-c2906"></a>Ошибка компилятора C2906

"специализация": для явной специализации требуется "Template <>"

Для явной специализации шаблонов необходимо использовать новый синтаксис.

Следующий пример приводит к возникновению ошибки C2906:

```cpp
// C2906.cpp
// compile with: /c
template<class T> class X{};   // primary template
class X<int> { }   // C2906
template<> class X<int> { };   // new syntax
```
