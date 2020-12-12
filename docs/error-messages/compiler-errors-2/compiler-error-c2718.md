---
description: 'Дополнительные сведения о: Ошибка компилятора C2718'
title: Ошибка компилятора C2718
ms.date: 11/04/2016
f1_keywords:
- C2718
helpviewer_keywords:
- C2718
ms.assetid: 78cc71f8-c142-46fc-9aed-970635d74f0c
ms.openlocfilehash: ab0ddd8f5afa8cc72259f527d0bb8731fa4e9a5a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320789"
---
# <a name="compiler-error-c2718"></a>Ошибка компилятора C2718

"параметр": фактический параметр с __declspec (выровняйте ("#")) не будет согласован

Использование [](../../cpp/align-cpp.md) **`__declspec`** модификатора aligned в параметрах функции не допускается.

Следующий пример приводит к возникновению ошибки C2718:

```cpp
// C2718.cpp
typedef struct __declspec(align(32)) AlignedStruct  {
   int i;
} AlignedStruct;

void f2(int i, ...);

void f4() {
   AlignedStruct as;

   f2(0, as);   // C2718, actual parameter is aligned
}
```
