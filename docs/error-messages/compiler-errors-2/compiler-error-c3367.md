---
description: 'Дополнительные сведения о: Ошибка компилятора C3367'
title: Ошибка компилятора C3367
ms.date: 11/04/2016
f1_keywords:
- C3367
helpviewer_keywords:
- C3367
ms.assetid: e675d42b-f5b0-4d43-aab1-1f5024233102
ms.openlocfilehash: cd428bb0472ab9cb621f85ac684cbb4d9bbc12d6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245282"
---
# <a name="compiler-error-c3367"></a>Ошибка компилятора C3367

"функция_статического_члена": невозможно использовать статическую функцию для создания несвязанного делегата

При вызове несвязанного делегата необходимо передать экземпляр объекта. Так как статическая функция-член вызывается через имя класса, с помощью функции-члена экземпляра можно создать только несвязанный делегат.

Дополнительные сведения о непривязанных делегатах см. [в разделе инструкции. Определение и использование делегатов (C++/CLI)](../../dotnet/how-to-define-and-use-delegates-cpp-cli.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3367.

```cpp
// C3367.cpp
// compile with: /clr
ref struct R {
   void b() {}
   static void f() {}
};

delegate void Del(R^);

int main() {
   Del ^ a = gcnew Del(&R::b);   // OK
   Del ^ b = gcnew Del(&R::f);   // C3367
}
```
