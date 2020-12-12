---
description: 'Дополнительные сведения о: Ошибка компилятора C2141'
title: Ошибка компилятора C2141
ms.date: 11/04/2016
f1_keywords:
- C2141
helpviewer_keywords:
- C2141
ms.assetid: 10cf770f-0500-4220-ac90-a863b7ea5fe6
ms.openlocfilehash: ea80cd02b3a7ec213b7b6d0eb3c0c1d4d94298b8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97270944"
---
# <a name="compiler-error-c2141"></a>Ошибка компилятора C2141

переполнение размера массива

Размер массива превышает ограничение в 2 ГБ. Уменьшите размер массива.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2141.

```cpp
// C2141.cpp
// processor: IPF
class A {
   short m_n;
};

int main()
{
   A* pA = (A*)(-1);
   pA = new A[0x8000000000000001];   // C2141

   A* pA2 = (A*)(-1);
   pA2 = new A[0x80000000000000F];   // OK
}
```
