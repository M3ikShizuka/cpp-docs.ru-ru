---
description: 'Дополнительные сведения о: Ошибка компилятора C3628'
title: Ошибка компилятора C3628
ms.date: 11/04/2016
f1_keywords:
- C3628
helpviewer_keywords:
- C3628
ms.assetid: 0ff5a4a4-fcc9-47a0-a4d8-8af9cf2815f6
ms.openlocfilehash: ed0c434a40e6c513580e37b5fb2fc9f44b1dc5dc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144408"
---
# <a name="compiler-error-c3628"></a>Ошибка компилятора C3628

"базовый класс": Managed или Винртклассес поддерживают только открытое наследование

Предпринята попытка использовать класс Managed или WinRT в качестве [закрытого](../../cpp/private-cpp.md) или [защищенного](../../cpp/protected-cpp.md) базового класса. Класс Managed или WinRT можно использовать только в качестве базового класса с [открытым](../../cpp/public-cpp.md) доступом.

В следующем примере показано возникновение ошибки C3628 и приводятся сведения по ее устранению.

```cpp
// C3628a.cpp
// compile with: /clr
ref class B {
};

ref class D : private B {   // C3628

// The following line resolves the error.
// ref class D : public B {
};

int main() {
}
```
