---
description: 'Дополнительные сведения о: Ошибка компилятора C3213'
title: Ошибка компилятора C3213
ms.date: 11/04/2016
f1_keywords:
- C3213
helpviewer_keywords:
- C3213
ms.assetid: 1f079e36-b3e9-40f8-8e95-08eeba3adc82
ms.openlocfilehash: 5ae16ffd94c6d300956bb2723ccbe8c16b0d6b3a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97291770"
---
# <a name="compiler-error-c3213"></a>Ошибка компилятора C3213

базовый класс "базовый_тип" менее доступен, чем "производный_тип"

Тип, который будет видимым из сборки, должен использовать публично видимые базовые классы.

В следующем примере возникает ошибка C3213:

```cpp
// C3213.cpp
// compile with: /clr
private ref struct privateG {
public:
   int i;
};

public ref struct publicG {
public:
   int i;
};

public ref struct V : public privateG {   // C3213
public:
   int j;
};

public ref struct W: public publicG {   // OK
public:
   int j;
};
```
