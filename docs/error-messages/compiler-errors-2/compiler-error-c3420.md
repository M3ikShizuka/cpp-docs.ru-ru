---
description: 'Дополнительные сведения о: Ошибка компилятора C3420'
title: Ошибка компилятора C3420
ms.date: 11/04/2016
f1_keywords:
- C3420
helpviewer_keywords:
- C3420
ms.assetid: 99b53c77-f36b-4574-9199-b53111becccb
ms.openlocfilehash: 3c79693823255ed7335e5805c0ac17de5ddcead7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316004"
---
# <a name="compiler-error-c3420"></a>Ошибка компилятора C3420

"метод_завершения": метод завершения не может быть виртуальным

Метод завершения можно вызвать только не виртуально из его включающего типа. Следовательно, это ошибка для объявления виртуального метода завершения.

Дополнительные сведения см. [в разделе Деструкторы и методы завершения в статье инструкции: определение и использование классов и структур (C++/CLI)](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Destructors_and_finalizers).

## <a name="example"></a>Пример

При компиляции следующего примера возникнет ошибка C3420.

```cpp
// C3420.cpp
// compile with: /clr /c
ref class R {
   virtual !R() {}   // C3420
};
```
