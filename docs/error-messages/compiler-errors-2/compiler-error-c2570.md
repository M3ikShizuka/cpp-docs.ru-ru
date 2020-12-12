---
description: 'Дополнительные сведения о: Ошибка компилятора C2570'
title: Ошибка компилятора C2570
ms.date: 11/04/2016
f1_keywords:
- C2570
helpviewer_keywords:
- C2570
ms.assetid: d65d0b32-2fac-464a-bcdf-0ebcedf3bf32
ms.openlocfilehash: faebc117991262c8fff94ef75f18d6e59c884315
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209026"
---
# <a name="compiler-error-c2570"></a>Ошибка компилятора C2570

"идентификатор": объединение не может иметь базовые классы

Объединение является производным от класса, структуры или объединения. Это не допускается. Вместо этого объявите производный тип как класс или структуру.

Следующий пример приводит к возникновению ошибки C2570:

```cpp
// C2570.cpp
// compile with: /c
class base {};
union hasPubBase : public base {};   // C2570
union hasNoBase {};   // OK
```
