---
description: 'Дополнительные сведения о: Ошибка компилятора C2785'
title: Ошибка компилятора C2785
ms.date: 11/04/2016
f1_keywords:
- C2785
helpviewer_keywords:
- C2785
ms.assetid: d8d13360-0d00-4815-8475-b49c7f0dc0f3
ms.openlocfilehash: f40b652e30b30f0ef17426b547337352181383e0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297906"
---
# <a name="compiler-error-c2785"></a>Ошибка компилятора C2785

"объявление1" и "объявление2" имеют различные возвращаемые типы

Тип возвращаемого значения специализации шаблона функции отличается от типа возвращаемого значения шаблона основной функции.

### <a name="to-correct-this-error"></a>Исправление ошибки

1. Проверьте все специализации шаблона функции на согласованность.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2785:

```cpp
// C2785.cpp
// compile with: /c
template<class T> void f(T);

template<> int f(int); // C2785
template<> void f(int); // OK
```
