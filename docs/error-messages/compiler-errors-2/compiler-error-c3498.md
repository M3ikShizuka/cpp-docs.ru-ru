---
description: 'Дополнительные сведения о: Ошибка компилятора C3498'
title: Ошибка компилятора C3498
ms.date: 11/04/2016
f1_keywords:
- C3498
helpviewer_keywords:
- C3498
ms.assetid: 0a5a7817-0872-4119-83bf-980a19113374
ms.openlocfilehash: f4d4ccb67494eb2d2cab499c210d360415fa9779
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97113106"
---
# <a name="compiler-error-c3498"></a>Ошибка компилятора C3498

"var": невозможно записать переменную с управляемым или Винрттипе

Нельзя записать переменную, имеющую управляемый тип или тип среды выполнения Windows в лямбда-выражении.

### <a name="to-correct-this-error"></a>Исправление ошибки

- Передайте управляемую переменную или переменную среды выполнения Windows в список параметров лямбда-выражения.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C3498, так как переменная, имеющая управляемый тип, присутствует в списке записи лямбда-выражения:

```cpp
// C3498a.cpp
// compile with: /clr
using namespace System;

int main()
{
   String ^ s = "Hello";
   [&s](String ^ r)
      { return String::Concat(s, r); } (", World!"); // C3498
}
```

Следующий пример разрешает C3498, передав управляемую переменную `s` в список параметров лямбда-выражения:

```cpp
// C3498b.cpp
// compile with: /clr
using namespace System;

int main()
{
   String ^ s = "Hello";
   [](String ^ s, String ^ r)
      { return String::Concat(s, r); } (s, ", World!");
}
```

## <a name="see-also"></a>См. также

[Лямбда-выражения](../../cpp/lambda-expressions-in-cpp.md)
