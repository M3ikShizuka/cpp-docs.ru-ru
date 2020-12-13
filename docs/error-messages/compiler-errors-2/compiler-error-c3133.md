---
description: 'Дополнительные сведения о: Ошибка компилятора C3133'
title: Ошибка компилятора C3133
ms.date: 11/04/2016
f1_keywords:
- C3133
helpviewer_keywords:
- C3133
ms.assetid: 4a709405-b67b-4061-8a2a-19fa5fb34a2a
ms.openlocfilehash: 3559e5864ea5f8d5e690a77899d6314ee2b65519
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97177384"
---
# <a name="compiler-error-c3133"></a>Ошибка компилятора C3133

Атрибуты не могут применяться к атрибутам C++ varargs

Атрибут был применен неправильно. Атрибуты не могут быть применены к многоточию, представляющему переменные аргументы.

Для получения дополнительной информации см. [User-Defined Attributes](../../extensions/user-defined-attributes-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3133.

```cpp
// C3133.cpp
// compile with: /clr /c
ref struct MyAttr: System::Attribute {};
void Func([MyAttr]...);   // C3133
void Func2([MyAttr] int i);   // OK
```
