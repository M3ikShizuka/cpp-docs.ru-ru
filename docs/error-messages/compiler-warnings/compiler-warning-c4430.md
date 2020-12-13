---
description: 'Дополнительные сведения о: предупреждение компилятора C4430'
title: Предупреждение компилятора C4430
ms.date: 11/04/2016
f1_keywords:
- C4430
helpviewer_keywords:
- C4430
ms.assetid: 12efbfff-aa58-4a86-a7d6-2c6a12d01dd3
ms.openlocfilehash: af214bb0e9d373ee319008f509ba78f5d7ade38b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344306"
---
# <a name="compiler-warning-c4430"></a>Предупреждение компилятора C4430

отсутствует спецификатор типа — предполагается int. Примечание. C++ не поддерживает int по умолчанию

Эта ошибка может быть вызвана работой по согласованности компилятора, выполненной для Visual Studio 2005: все объявления должны явно указывать тип. int больше не предполагается.

C4430 всегда выдается как ошибка.  Это предупреждение можно отключить с помощью `#pragma warning` или **/WD**; см. [предупреждение](../../preprocessor/warning.md) или [/W,/W0,/W1,/W2,/W3,/W4,/W1,/W2,/W3,/W4,/Wall,/WD,/We,/WO,/WV,/WX (уровень предупреждений)](../../build/reference/compiler-option-warning-level.md) для получения дополнительных сведений.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4430.

```cpp
// C4430.cpp
// compile with: /c
struct CMyClass {
   CUndeclared m_myClass;  // C4430
   int m_myClass;  // OK
};

typedef struct {
   POINT();   // C4430
   // try the following line instead
   // int POINT();
   unsigned x;
   unsigned y;
} POINT;
```
