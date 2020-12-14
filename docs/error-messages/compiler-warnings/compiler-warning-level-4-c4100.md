---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4100'
title: Предупреждение компилятора (уровень 4) C4100
ms.date: 11/04/2016
f1_keywords:
- C4100
helpviewer_keywords:
- C4100
ms.assetid: 478ed97d-e502-49e4-9afb-ac2a6c61194b
ms.openlocfilehash: 753be5e6e56e4ad94d6b742454fe62e303d430dd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97262000"
---
# <a name="compiler-warning-level-4-c4100"></a>Предупреждение компилятора (уровень 4) C4100

"идентификатор": формальный параметр без ссылки

В теле функции отсутствует ссылка на формальный параметр. Параметр без ссылки игнорируется.

C4100 также можно выдавать, когда код вызывает деструктор для параметра-примитива, не ссылающегося на другой тип.  Это ограничение относится к компилятору Microsoft C++.

Следующий пример приводит к возникновению ошибки C4100:

```cpp
// C4100.cpp
// compile with: /W4
void func(int i) {   // C4100, delete the unreferenced parameter to
                     //resolve the warning
   // i;   // or, add a reference like this
}

int main()
{
   func(1);
}
```
