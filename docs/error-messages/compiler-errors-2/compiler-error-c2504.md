---
description: 'Дополнительные сведения о: Ошибка компилятора C2504'
title: Ошибка компилятора C2504
ms.date: 11/04/2016
f1_keywords:
- C2504
helpviewer_keywords:
- C2504
ms.assetid: c9e002a6-a4ee-4ba7-970e-edf4adb83692
ms.openlocfilehash: 2a2269d750673a912096b497c10a9b112c23207c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97213030"
---
# <a name="compiler-error-c2504"></a>Ошибка компилятора C2504

"класс": базовый класс не определен

Базовый класс объявлен, но не определен.  Возможные причины.

1. Отсутствует включаемый файл.

1. Внешний базовый класс не объявлен с [модификатором extern](../../cpp/extern-cpp.md).

Следующий пример приводит к возникновению ошибки C2504:

```cpp
// C2504.cpp
// compile with: /c
class A;
class B : public A {};   // C2504
```

Хорошо

```
class C{};
class D : public C {};
```
