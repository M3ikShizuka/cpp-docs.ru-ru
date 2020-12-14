---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4829'
title: Предупреждение компилятора (уровень 1) C4829
ms.date: 11/04/2016
f1_keywords:
- C4829
helpviewer_keywords:
- C4829
ms.assetid: 4ffabe2b-2ddc-4c52-8564-d1355c93cfa6
ms.openlocfilehash: ae44c50e7b680dff94427896eea2e10c4ed33483
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97198028"
---
# <a name="compiler-warning-level-1-c4829"></a>Предупреждение компилятора (уровень 1) C4829

Возможно, неверные параметры для функции main. Рассмотрим "интмаин (Platform:: array \<Platform::String^> ^ argv)"

Некоторые функции, например main, не могут принимать параметры ссылочного типа. Хотя компиляция будет успешной, полученный в результате образ, возможно, не будет выполняться.

Следующий пример приводит к возникновению ошибки C4829.

```cpp
// C4829.cpp
// compile by using: cl /EHsc /ZW /W4 /c C4829.cpp
int main(Platform::String ^ s) {}   // C4829
```
