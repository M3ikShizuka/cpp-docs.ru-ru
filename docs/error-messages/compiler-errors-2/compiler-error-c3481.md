---
description: 'Дополнительные сведения о: Ошибка компилятора C3481'
title: Ошибка компилятора C3481
ms.date: 11/04/2016
f1_keywords:
- C3481
helpviewer_keywords:
- C3481
ms.assetid: 5d09375a-5ed3-4b61-86ed-45e91fd734c7
ms.openlocfilehash: 31f13b56a2b5df66a5765ee63313ffe265c15fe4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97113406"
---
# <a name="compiler-error-c3481"></a>Ошибка компилятора C3481

var: переменная, передаваемая в лямбда-выражение, не найдена

Компилятору не удалось найти определение переменной, которая передается в список передаваемых параметров в лямбда-выражении.

### <a name="to-correct-this-error"></a>Исправление ошибки

- Удалите переменную из списка передаваемых параметров в лямбда-выражении.

## <a name="example"></a>Пример

В следующем примере возникает ошибка C3481, так как переменная `n` не определена:

```cpp
// C3481.cpp

int main()
{
   [n] {}(); // C3481
}
```

## <a name="see-also"></a>См. также

[Лямбда-выражения](../../cpp/lambda-expressions-in-cpp.md)
