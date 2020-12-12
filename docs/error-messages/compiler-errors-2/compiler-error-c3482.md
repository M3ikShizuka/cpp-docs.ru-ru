---
description: 'Дополнительные сведения о: Ошибка компилятора C3482'
title: Ошибка компилятора C3482
ms.date: 11/04/2016
f1_keywords:
- C3482
helpviewer_keywords:
- C3482
ms.assetid: bf99558e-bef4-421c-bb16-dcd9c54c1011
ms.openlocfilehash: 752ce53b590ef5c10c25e0d0e850c7c4cc2776bf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97315703"
---
# <a name="compiler-error-c3482"></a>Ошибка компилятора C3482

"this" может быть использован в качестве передаваемого параметра в лямбда-выражении только с нестатической функцией-членом

Нельзя передать в **`this`** список записи лямбда-выражения, объявленного в статическом методе или глобальной функции.

### <a name="to-correct-this-error"></a>Исправление ошибки

- Преобразуйте включающую функцию в нестатический метод или

- Удалите **`this`** указатель из списка записи лямбда-выражения.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению предупреждения C3482:

```cpp
// C3482.cpp
// compile with: /c

class C
{
public:
   static void staticMethod()
   {
      [this] {}(); // C3482
   }
};
```

## <a name="see-also"></a>См. также

[Лямбда-выражения](../../cpp/lambda-expressions-in-cpp.md)
