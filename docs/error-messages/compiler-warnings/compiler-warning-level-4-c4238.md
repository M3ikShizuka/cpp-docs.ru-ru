---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4238'
title: Предупреждение компилятора (уровень 4) C4238
ms.date: 11/04/2016
f1_keywords:
- C4238
helpviewer_keywords:
- C4238
ms.assetid: 5d4051d3-7b0f-43ea-8c8d-d194bfdceb71
ms.openlocfilehash: 8999d9ebeb4583256360f6223d4bf51a842fcb01
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334870"
---
# <a name="compiler-warning-level-4-c4238"></a>Предупреждение компилятора (уровень 4) C4238

использовано нестандартное расширение: rvalue класса используется как lvalue

Для совместимости с предыдущими версиями Visual C++ расширения Майкрософт (**/Ze**) позволяют использовать тип класса в качестве rvalue в контексте, который неявно или явно принимает свой адрес. В некоторых случаях, например в приведенном ниже примере, это может быть опасно.

## <a name="example"></a>Пример

```cpp
// C4238.cpp
// compile with: /W4 /c
struct C {
   C() {}
};

C * pC = &C();   // C4238
```

Это использование приводит к ошибке при совместимости с ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).
