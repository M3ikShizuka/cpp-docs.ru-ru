---
description: 'Дополнительные сведения о: Ошибка компилятора C3536'
title: Ошибка компилятора C3536
ms.date: 11/04/2016
f1_keywords:
- C3536
helpviewer_keywords:
- C3536
ms.assetid: 8d866075-866b-49eb-9979-ee27b308f7e3
ms.openlocfilehash: 62bd8bb75adfbf0e21f150f4240bb5f4011f6382
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97112509"
---
# <a name="compiler-error-c3536"></a>Ошибка компилятора C3536

"символ": не может использоваться до инициализации

Указанный символ не может быть использован до инициализации. Практически это означает, что переменную нельзя использовать для инициализации самой себя.

### <a name="to-correct-this-error"></a>Исправление ошибки

1. Не инициализируйте переменную с самой себя.

## <a name="example"></a>Пример

В следующем примере создается C3536, так как каждая переменная инициализируется сама по себе.

```cpp
// C3536.cpp
// Compile with /Zc:auto
int main()
{
   auto a = a;     //C3536
   auto b = &b;    //C3536
   auto c = c + 1; //C3536
   auto* d = &d;   //C3536
   auto& e = e;    //C3536
   return 0;
};
```

## <a name="see-also"></a>См. также

[Ключевое слово auto](../../cpp/auto-cpp.md)
