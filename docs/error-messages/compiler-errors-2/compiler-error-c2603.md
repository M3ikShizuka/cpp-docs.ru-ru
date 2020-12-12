---
description: 'Дополнительные сведения о: Ошибка компилятора C2603'
title: Ошибка компилятора C2603
ms.date: 11/04/2016
f1_keywords:
- C2603
helpviewer_keywords:
- C2603
ms.assetid: 9ca520d0-f082-4b65-933d-17c3bcf8b02c
ms.openlocfilehash: e28ea581c4c1417972cddc0ce558bd518acb8889
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97208792"
---
# <a name="compiler-error-c2603"></a>Ошибка компилятора C2603

> "*функция*": слишком много статических объектов области действия блока с конструктором или деструктором в функции

В версиях компилятора Microsoft C++ до Visual Studio 2015 или при указании параметра [/Zc: threadSafeInit-](../../build/reference/zc-threadsafeinit-thread-safe-local-static-initialization.md) Compiler существует ограничение в 31 на число статических объектов, которые можно использовать во встроенной функции, видимой извне.

Чтобы устранить эту проблему, рекомендуется использовать более позднюю версию набора инструментов компилятора Microsoft C++ или, если это возможно, удалить параметр/Zc: threadSafeInit-Compiler. Если это невозможно, рассмотрите возможность объединения статических объектов. Если объекты имеют один и тот же тип, рекомендуется использовать один статический массив этого типа и ссылаться на отдельные элементы по мере необходимости.

## <a name="example"></a>Пример

Следующий код создает C2603 и показывает один из способов его исправления:

```cpp
// C2603.cpp
// Compile by using: cl /W4 /c /Zc:threadSafeInit- C2603.cpp
struct C { C() {} };
extern inline void f1() {
    static C C01, C02, C03, C04, C05, C06, C07, C08, C09, C10;
    static C C11, C12, C13, C14, C15, C16, C17, C18, C19, C20;
    static C C21, C22, C23, C24, C25, C26, C27, C28, C29, C30, C31;
    static C C32;   // C2603 Comment this line out to avoid error
}
```
