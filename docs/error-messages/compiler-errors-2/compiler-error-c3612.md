---
description: 'Дополнительные сведения о: Ошибка компилятора C3612'
title: Ошибка компилятора C3612
ms.date: 11/04/2016
f1_keywords:
- C3612
helpviewer_keywords:
- C3612
ms.assetid: aa6e3a2b-4afa-481c-98c1-1b6d1f82f869
ms.openlocfilehash: 332d4bae940a0c98b148fd6ba951a4f51d1bee27
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97223104"
---
# <a name="compiler-error-c3612"></a>Ошибка компилятора C3612

"тип": запечатанный класс не может быть абстрактным

Типы, определенные с помощью, `value` по умолчанию запечатаны, а класс является абстрактным, если только он не реализует все методы его базового класса. Запечатанный абстрактный класс не может быть базовым классом и не может быть создан.

Дополнительные сведения см. в статье [Классы и структуры](../../extensions/classes-and-structs-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3612:

```cpp
// C3612.cpp
// compile with: /clr /c
value struct V: public System::ICloneable {};   // C3612

// OK
value struct V2: public System::ICloneable {
   Object^ Clone();
};
```
