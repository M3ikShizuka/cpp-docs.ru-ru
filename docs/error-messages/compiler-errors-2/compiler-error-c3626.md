---
description: 'Дополнительные сведения о: Ошибка компилятора C3626'
title: Ошибка компилятора C3626
ms.date: 11/04/2016
f1_keywords:
- C3626
helpviewer_keywords:
- C3626
ms.assetid: 43926e2b-1ba9-4a43-9343-c58449cbb336
ms.openlocfilehash: 8db976a5f072db618ac4270df3bd1d8edf0ab15c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144421"
---
# <a name="compiler-error-c3626"></a>Ошибка компилятора C3626

"ключевое слово": ключевое слово "__event" можно использовать только в интерфейсах COM, функциях-членах и элементах данных, которые являются указателями на делегаты

Ключевое слово было использовано неправильно.

Следующий пример приводит к возникновению ошибки C3626:

```cpp
// C3626.cpp
// compile with: /c
struct A {
   __event int i;   // C3626
// try the following line instead
// __event int i();
};
```
