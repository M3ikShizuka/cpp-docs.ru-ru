---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4537'
title: Предупреждение компилятора (уровень 1) C4537
ms.date: 08/27/2018
f1_keywords:
- C4537
helpviewer_keywords:
- C4537
ms.assetid: 9454493c-d419-475e-8f35-9c00233c9329
ms.openlocfilehash: 39219361445832f51160311733c77d3becd8bc5f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294773"
---
# <a name="compiler-warning-level-1-c4537"></a>Предупреждение компилятора (уровень 1) C4537

> "*объект*": "*оператор*" применяется к типу, не являющемуся UDT

## <a name="remarks"></a>Комментарии

Была передана ссылка, где ожидался объект (определяемый пользователем тип). Ссылка не является объектом, но встроенный код ассемблера не может сделать различие. Компилятор создает код, как будто *объект* являлся экземпляром.

## <a name="example"></a>Пример

В следующем примере создается C4537 и демонстрируется его устранение.

```cpp
// C4537.cpp
// compile with: /W1 /c
// processor: x86
struct S {
    int member;
};

void f1(S &s) {
    __asm mov eax, s.member;   // C4537
    // try the following code instead
    // or, make the declaration "void f1(S s)"
    /*
    mov eax, s
    mov eax, [eax]s.member
    */
}
```
