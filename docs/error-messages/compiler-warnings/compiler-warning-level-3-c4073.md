---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4073'
title: Предупреждение компилятора (уровень 3) C4073
ms.date: 11/04/2016
f1_keywords:
- C4073
helpviewer_keywords:
- C4073
ms.assetid: 50081a6e-6acd-45ff-8484-9b1ea926cc5c
ms.openlocfilehash: a276dbb4c421eb828f80dde25bb2249e217e5df2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97208558"
---
# <a name="compiler-warning-level-3-c4073"></a>Предупреждение компилятора (уровень 3) C4073

инициализаторы, помещаемые в область инициализации библиотеки

Только разработчики библиотек сторонних разработчиков должны использовать область инициализации библиотеки, которая указывается [#pragma init_seg](../../preprocessor/init-seg.md). Следующий пример приводит к возникновению ошибки C4073:

```cpp
// C4073.cpp
// compile with: /W3
#pragma init_seg(lib)   // C4073

// try this line to resolve the warning
// #pragma init_seg(user)

int main() {
}
```
