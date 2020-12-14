---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4208'
title: Предупреждение компилятора (уровень 4) C4208
ms.date: 11/04/2016
f1_keywords:
- C4208
helpviewer_keywords:
- C4208
ms.assetid: 5cb0a36e-3fb5-422f-a5f9-e40b70776c27
ms.openlocfilehash: a99e9435fcdbfb65248fb38883a8f3395ef4db14
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314780"
---
# <a name="compiler-warning-level-4-c4208"></a>Предупреждение компилятора (уровень 4) C4208

использовано нестандартное расширение: Delete [exp]-exp вычислено, но пропущено

С помощью расширений Майкрософт (/Ze) можно удалить массив, используя значение в квадратных скобках с [оператором delete](../../cpp/delete-operator-cpp.md). Значение игнорируется.

```cpp
// C4208.cpp
// compile with: /W4
int main()
{
   int * MyArray = new int[18];
   delete [18] MyArray;      // C4208
   MyArray = new int[18];
   delete [] MyArray;        // ok
}
```

Такие значения недопустимы в режиме совместимости ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).
