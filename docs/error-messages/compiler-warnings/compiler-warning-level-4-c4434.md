---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4434'
title: Предупреждение компилятора (уровень 4) C4434
ms.date: 11/04/2016
f1_keywords:
- C4434
helpviewer_keywords:
- C4434
ms.assetid: 24b8785e-353a-4c37-8bed-ed61001a871d
ms.openlocfilehash: 24e8066ec415293eddf6de1d5a2dd2644623f2ac
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251470"
---
# <a name="compiler-warning-level-4-c4434"></a>Предупреждение компилятора (уровень 4) C4434

Конструктор класса должен иметь закрытый уровень доступности; изменение на частный доступ

C4434 указывает, что компилятор изменил доступность статического конструктора. Статические конструкторы должны иметь закрытый уровень доступности, так как они предназначены только для вызова средой CLR. Дополнительные сведения см. в разделе [Статические конструкторы](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Static_constructors).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4434.

```cpp
// C4434.cpp
// compile with: /W4 /c /clr
public ref struct R {
   static R(){}   // C4434
};
```
