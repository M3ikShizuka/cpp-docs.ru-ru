---
description: 'Дополнительные сведения о: Ошибка компилятора C3496'
title: Ошибка компилятора C3496
ms.date: 11/04/2016
f1_keywords:
- C3496
helpviewer_keywords:
- C3496
ms.assetid: e19885f2-677f-4c1e-bc69-e35852262dc3
ms.openlocfilehash: dc3160e1007b65b70ea952aeaee3c77ba8ab21e6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97315521"
---
# <a name="compiler-error-c3496"></a>Ошибка компилятора C3496

"this" всегда передается по значению: знак "&" проигнорирован

Невозможно захватить **`this`** указатель по ссылке.

### <a name="to-correct-this-error"></a>Исправление ошибки

- Зафиксируйте **`this`** указатель по значению.

## <a name="example"></a>Пример

В следующем примере создается C3496, так как ссылка на **`this`** указатель появляется в списке записи лямбда-выражения:

```cpp
// C3496.cpp
// compile with: /c

class C
{
   void f()
   {
      [&this] {}(); // C3496
   }
};
```

## <a name="see-also"></a>См. также

[Лямбда-выражения](../../cpp/lambda-expressions-in-cpp.md)
