---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4144'
title: Предупреждение компилятора (уровень 1) C4144
ms.date: 11/04/2016
f1_keywords:
- C4144
helpviewer_keywords:
- C4144
ms.assetid: a37b445d-dbc6-43b4-8d95-ffd0e4225464
ms.openlocfilehash: 11f276d4790c11654655fea7cf814dfb30a6787b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97136309"
---
# <a name="compiler-warning-level-1-c4144"></a>Предупреждение компилятора (уровень 1) C4144

"выражение": выражение отношения в качестве выражения switch

Указанное реляционное выражение было использовано в качестве управляющего выражения оператора [switch](../../cpp/switch-statement-cpp.md) . Связанные инструкции CASE будут предлагать логические значения. Следующий пример приводит к возникновению ошибки C4144:

```cpp
// C4144.cpp
// compile with: /W1
int main()
{
   int i = 0;
   switch(!i) {   // C4144, remove the ! to resolve
      case 1:
         break;
      default:
         break;
   }
}
```
