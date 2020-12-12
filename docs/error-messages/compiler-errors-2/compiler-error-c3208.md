---
description: 'Дополнительные сведения о: Ошибка компилятора C3208'
title: Ошибка компилятора C3208
ms.date: 11/04/2016
f1_keywords:
- C3208
helpviewer_keywords:
- C3208
ms.assetid: 6d060bfe-52cf-4599-8f70-bdeb5a670df3
ms.openlocfilehash: bd76a209fa3736449e8816473d0dee12daa93a61
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97173952"
---
# <a name="compiler-error-c3208"></a>Ошибка компилятора C3208

"функция": список параметров шаблона для класса-шаблона "класс" не совпадает со списком параметров шаблона для параметра шаблона "параметр"

Параметр шаблона template и предоставленный класс-шаблон имеют разное количество параметров шаблона.

Следующий пример приводит к возникновению ошибки C3208:

```cpp
// C3208.cpp
template <template <class T> class TT >
int f();

template <class T1, class T2>
struct S;

template <class T1>
struct R;

int i = f<S>();   // C3208
// try the following line instead
// int i = f<R>();
```
