---
description: 'Дополнительные сведения о: Ошибка компилятора C3375'
title: Ошибка компилятора C3375
ms.date: 11/04/2016
f1_keywords:
- C3375
helpviewer_keywords:
- C3375
ms.assetid: f1df78c6-e6ca-48f3-8b29-4e1710002bf3
ms.openlocfilehash: d2a9e9904185877e730096d08cb1f7c23c35c0d2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335001"
---
# <a name="compiler-error-c3375"></a>Ошибка компилятора C3375

"функция": неоднозначная функция делегата

Создание экземпляра делегата могло быть выполнено в статической функции-члене или как непривязанного делегата для функции экземпляра, поэтому компилятор выдал данную ошибку.

Дополнительные сведения см. в разделе [Delegate (расширения компонентов C++)](../../extensions/delegate-cpp-component-extensions.md).

## <a name="example"></a>Пример

В следующем примере возникает ошибка C3375:

```cpp
// C3375.cpp
// compile with: /clr
ref struct R {
   static void f(R^) {}
   void f() {}
};

delegate void Del(R^);

int main() {
   Del ^ a = gcnew Del(&R::f);   // C3375
}
```
