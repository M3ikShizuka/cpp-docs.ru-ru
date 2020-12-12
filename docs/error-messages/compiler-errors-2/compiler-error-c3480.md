---
description: 'Дополнительные сведения о: Ошибка компилятора C3480'
title: Ошибка компилятора C3480
ms.date: 11/04/2016
f1_keywords:
- C3480
helpviewer_keywords:
- C3480
ms.assetid: 7b2e055a-9604-4d13-861b-b38bda1a6940
ms.openlocfilehash: dbeed462410d36b466e807d576549c1b73ee4917
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97113419"
---
# <a name="compiler-error-c3480"></a>Ошибка компилятора C3480

"переменная": передаваемая переменная в лямбда-выражении должна быть из внешней области видимости функции

Передаваемая переменная в лямбда-выражении не относится к внешней области видимости функции.

### <a name="to-correct-this-error"></a>Исправление ошибки

- Удалите переменную из списка передаваемых параметров в лямбда-выражении.

## <a name="examples"></a>Примеры

Приведенный ниже пример вызывает ошибку C3480, так как переменная `global` не относится к внешней области видимости функции.

```cpp
// C3480a.cpp

int global = 0;
int main()
{
   [&global] { global = 5; }(); // C3480
}
```

В приведенном ниже примере ошибка C3480 устраняется путем удаления переменной `global` из списка передачи лямбда-выражения.

```cpp
// C3480b.cpp

int global = 0;
int main()
{
   [] { global = 5; }();
}
```

## <a name="see-also"></a>См. также

[Лямбда-выражения](../../cpp/lambda-expressions-in-cpp.md)
