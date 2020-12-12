---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4180'
title: Предупреждение компилятора (уровень 1) C4180
ms.date: 11/04/2016
f1_keywords:
- C4180
helpviewer_keywords:
- C4180
ms.assetid: 40c91bd4-37f1-4d59-a4f3-d5ddab68239b
ms.openlocfilehash: d85097212086d98b70b71837b01ef1522f87580c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97266719"
---
# <a name="compiler-warning-level-1-c4180"></a>Предупреждение компилятора (уровень 1) C4180

квалификатор, примененный к типу-функции, не имеет смысла; пропуск

Квалификатор, например **`const`** , применяется к типу функции, определенному параметром **`typedef`** .

## <a name="example"></a>Пример

```cpp
// C4180.cpp
// compile with: /W1 /c
typedef int FuncType(void);

// the const qualifier cannot be applied to the
// function type FuncType
const FuncType f;   // C4180
```
