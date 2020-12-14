---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4288'
title: Предупреждение компилятора (уровень 1) C4288
ms.date: 11/04/2016
f1_keywords:
- C4288
helpviewer_keywords:
- C4288
ms.assetid: 6aaeb139-90cd-457a-9d37-65687042736f
ms.openlocfilehash: 827dd357aa4504c9f806cbcbe534ae45ccaf33b5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97311725"
---
# <a name="compiler-warning-level-1-c4288"></a>Предупреждение компилятора (уровень 1) C4288

> нестандартное расширение: "var": переменная управления циклом, объявленная в цикле for, используется вне области действия цикла. он конфликтует с объявлением во внешней области видимости

При компиляции с помощью [`/Ze`](../../build/reference/za-ze-disable-language-extensions.md) и **/Zc: forScope-** переменная, объявленная в **`for`** цикле, была использована после [](../../cpp/for-statement-cpp.md)области действия цикла. Расширение Microsoft для языка C++ позволяет этой переменной остаться в области, а C4288 напоминает, что первое объявление переменной не используется.

[`/Zc:forScope`](../../build/reference/zc-forscope-force-conformance-in-for-loop-scope.md)Сведения о том, как указать расширение Майкрософт в **`for`** циклах с помощью параметром/Ze., см. в разделе.

Следующий пример приводит к возникновению ошибки C4288:

```cpp
// C4288.cpp
// compile with: /W1 /c /Zc:forScope-
int main() {
   int i = 0;    // not used in this program
   for (int i = 0 ; ; ) ;
   i++;   // C4288 using for-loop declaration of i
}
```
