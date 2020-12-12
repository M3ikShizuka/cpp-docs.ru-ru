---
description: 'Дополнительные сведения о: Ошибка компилятора C2811'
title: Ошибка компилятора C2811
ms.date: 11/04/2016
f1_keywords:
- C2811
helpviewer_keywords:
- C2811
ms.assetid: 6a44b18e-44c1-49d8-9b99-e0545b9a6e7d
ms.openlocfilehash: 02b4770b08bdfc9ee15386874ebba2265716536d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194856"
---
# <a name="compiler-error-c2811"></a>Ошибка компилятора C2811

"тип1": не может наследовать от "тип2", ссылочный класс может наследовать только от класса ссылки или класса интерфейса

Предпринята попытка использовать неуправляемый класс в качестве базового класса для управляемого класса.

Следующий пример приводит к возникновению ошибки C2811:

```cpp
// C2811.cpp
// compile with: /clr /c
struct S{};
ref struct T {};
ref class C : public S {};   // C2811
ref class D : public T {};   // OK
```
