---
description: 'Дополнительные сведения о: Ошибка компилятора C2086'
title: Ошибка компилятора C2086
ms.date: 11/04/2016
f1_keywords:
- C2086
helpviewer_keywords:
- C2086
ms.assetid: 4329bf72-90c8-444c-8524-4ef75e6b2139
ms.openlocfilehash: b98b4ed3896b11d8df434935c1b539f76640f24c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97252081"
---
# <a name="compiler-error-c2086"></a>Ошибка компилятора C2086

"идентификатор": переопределение

Идентификатор определен более одного раза, или последующее объявление отличается от предыдущего.

C2086 также может быть результатом инкрементного создания для упоминаемой сборки C#. Чтобы устранить эту ошибку, перестройте сборку C#.

Следующий пример приводит к возникновению ошибки C2086:

```cpp
// C2086.cpp
main() {
  int a;
  int a;   // C2086 not an error in ANSI C
}
```
