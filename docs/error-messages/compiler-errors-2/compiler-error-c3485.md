---
description: 'Дополнительные сведения о: Ошибка компилятора C3485'
title: Ошибка компилятора C3485
ms.date: 11/04/2016
f1_keywords:
- C3485
helpviewer_keywords:
- C3485
ms.assetid: d67536f9-67a1-4ad9-9a94-d8bbbca3d0dc
ms.openlocfilehash: 0b11eb4487a9b6deb611852dd11a8a1963dd961e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97168388"
---
# <a name="compiler-error-c3485"></a>Ошибка компилятора C3485

определение лямбда-выражения не может содержать cv-квалификаторы

Нельзя использовать **`const`** **`volatile`** квалификатор или как часть определения лямбда-выражения.

### <a name="to-correct-this-error"></a>Исправление ошибки

- Удалите **`const`** квалификатор или **`volatile`** из определения лямбда-выражения.

## <a name="example"></a>Пример

В следующем примере создается C3485, так как он использует **`const`** квалификатор как часть определения лямбда-выражения:

```cpp
// C3485.cpp

int main()
{
   auto x = []() const mutable {}; // C3485
}
```

## <a name="see-also"></a>См. также

[Лямбда-выражения](../../cpp/lambda-expressions-in-cpp.md)
