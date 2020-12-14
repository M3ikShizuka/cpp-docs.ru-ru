---
description: 'Дополнительные сведения о: Ошибка компилятора C2798'
title: Ошибка компилятора C2798
ms.date: 11/04/2016
f1_keywords:
- C2798
helpviewer_keywords:
- C2798
ms.assetid: fb0cd861-b228-4f81-8090-e28344a727e0
ms.openlocfilehash: d3a78eaf09797d658c64b5659dcd0e05191fab1c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297594"
---
# <a name="compiler-error-c2798"></a>Ошибка компилятора C2798

"Super:: member" является неоднозначным

Несколько унаследованных структур содержат член, на который имеется ссылка [Super](../../cpp/super.md). Эту ошибку можно исправить одним из следующих:

- Удаление B1 или B2 из списка наследования D.

- Изменение имени элемента данных в B1 или B2.

Следующий пример приводит к возникновению ошибки C2798:

```cpp
// C2798.cpp
struct B1 {
   int i;
};

struct B2 {
   int i;
};

struct D : B1, B2 {
   void g() {
      __super::i = 4; // C2798
   }
};
```
