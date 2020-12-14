---
description: 'Дополнительные сведения о: Ошибка компилятора C2500'
title: Ошибка компилятора C2500
ms.date: 11/04/2016
f1_keywords:
- C2500
helpviewer_keywords:
- C2500
ms.assetid: 6bff8161-dc9a-48ca-91f1-fd2eefdbbc93
ms.openlocfilehash: 39d1ab0876470b443d4444a3c583cc0993c98325
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97275975"
---
# <a name="compiler-error-c2500"></a>Ошибка компилятора C2500

"идентификатор1": "идентификатор2" уже является прямым базовым классом

Класс или структура встречается несколько раз в списке базовых классов.

Прямым основанием является одна из них, упомянутая в базовом списке. Косвенная база является базовым классом одного из классов в базовом списке.

Класс не может быть указан как прямой базовый класс более одного раза. Класс можно использовать в качестве косвенного базового класса более одного раза.

Следующий пример приводит к возникновению ошибки C2500:

```cpp
// C2500.cpp
// compile with: /c
class A {};
class B : public A, public A {};    // C2500

// OK
class C : public A {};
class D : public A {};
class E : public C, public D {};
```
