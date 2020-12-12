---
description: 'Дополнительные сведения о: Ошибка компилятора C3625'
title: Ошибка компилятора C3625
ms.date: 11/04/2016
f1_keywords:
- C3625
helpviewer_keywords:
- C3625
ms.assetid: fdf49f21-d6b1-42f4-9eec-23b04ae8b4aa
ms.openlocfilehash: ee28175eac35e05ca2a4620dffa84cf995e053a7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144499"
---
# <a name="compiler-error-c3625"></a>Ошибка компилятора C3625

native_type: неуправляемый тип не может быть производным от типа WinRT type

Неуправляемый класс не может наследовать от управляемого класса или класса WinRT. Дополнительные сведения см. в статье [Классы и структуры](../../extensions/classes-and-structs-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3625:

```cpp
// C3625.cpp
// compile with: /clr /c
ref class B {};
class D : public B {};   // C3625 cannot inherit from a managed class
```
