---
description: 'Дополнительные сведения о: Ошибка компилятора C2474'
title: Ошибка компилятора C2474
ms.date: 11/04/2016
f1_keywords:
- C2474
helpviewer_keywords:
- C2474
ms.assetid: 64e6c61e-6e77-480e-bcf0-b30a2fc482ac
ms.openlocfilehash: adbfce63a5a8d97707bfb8e73dfda265f5d5e328
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97164410"
---
# <a name="compiler-error-c2474"></a>Ошибка компилятора C2474

"ключевое_слово": отсутствует соседняя точка с запятой; может представлять ключевое слово или идентификатор

Компилятор ожидал встретить точку с запятой, ему не удалось определить ваше намерение. Добавьте точку с запятой, чтобы устранить эту ошибку.

## <a name="example"></a>Пример

При компиляции следующего примера возникнет ошибка C2474:

```cpp
// C2474.cpp
// compile with: /clr /c

ref class A {
   ref class B {}
   property int i;   // C2474 error
};

// OK
ref class B {
   ref class D {};
   property int i;
};

ref class E {
   ref class F {} property;
   int i;
};
```
