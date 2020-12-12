---
description: 'Дополнительные сведения о: Ошибка компилятора C2597'
title: Ошибка компилятора C2597
ms.date: 11/04/2016
f1_keywords:
- C2597
helpviewer_keywords:
- C2597
ms.assetid: 2e48127d-e3ff-4a40-8156-2863e45b1a38
ms.openlocfilehash: b3430da85cef961b7c26b55e8dee9f1911533faf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97120143"
---
# <a name="compiler-error-c2597"></a>Ошибка компилятора C2597

недопустимая ссылка на нестатический член identifier

Возможные причины.

1. Нестатический член используется в статической функции-члене. Для доступа к нестатическому члену необходимо передать или создать локальный экземпляр класса и использовать оператор доступа к члену (`.` или `->`).

1. Указанный идентификатор не является членом класса, структуры или объединения. Проверьте написание идентификатора.

1. Оператор доступа к члену ссылается на функцию, не являющуюся членом.

1. В следующем примере показано возникновение ошибки C2597 и приводятся сведения по ее устранению.

```cpp
// C2597.cpp
// compile with: /c
struct s1 {
   static void func();
   static void func2(s1&);
   int i;
};

void s1::func() {
   i = 1;    // C2597 - static function can't access non-static data member
}

// OK - fix by passing an instance of s1
void s1::func2(s1& a) {
   a.i = 1;
}
```
