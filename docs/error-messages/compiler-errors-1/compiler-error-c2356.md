---
description: 'Дополнительные сведения о: Ошибка компилятора C2356'
title: Ошибка компилятора C2356
ms.date: 11/04/2016
f1_keywords:
- C2356
helpviewer_keywords:
- C2356
ms.assetid: 84d5a816-9a61-4d45-9978-38e485bbf767
ms.openlocfilehash: c0e2d179bb41e6cbae674d92976674ab90f05c0f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97328325"
---
# <a name="compiler-error-c2356"></a>Ошибка компилятора C2356

сегмент инициализации не должен изменяться во время записи преобразования

Возможные причины.

- `#pragma init_seg` предшествует код инициализации сегмента

- `#pragma init_seg` предшествует другому `#pragma init_seg`

Чтобы устранить эту проблему, переместите код инициализации сегмента в начало модуля. Если необходимо инициализировать несколько областей, переместите их в отдельные модули.

Следующий пример приводит к возникновению ошибки C2356:

```cpp
// C2356.cpp
#pragma warning(disable : 4075)

int __cdecl myexit(void (__cdecl *)());
int __cdecl myexit2(void (__cdecl *)());

#pragma init_seg(".mine$m",myexit)
#pragma init_seg(".mine$m",myexit2)   // C2356
```
