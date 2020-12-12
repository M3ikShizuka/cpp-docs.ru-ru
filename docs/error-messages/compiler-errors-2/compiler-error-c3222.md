---
description: 'Дополнительные сведения о: Ошибка компилятора C3222'
title: Ошибка компилятора C3222
ms.date: 11/04/2016
f1_keywords:
- C3222
helpviewer_keywords:
- C3222
ms.assetid: 5624bde8-2fd0-4b8b-92ce-5dfbaf91cf93
ms.openlocfilehash: 77883b6bd9be034fff2a0bcf3babdb1489c9a937
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97267720"
---
# <a name="compiler-error-c3222"></a>Ошибка компилятора C3222

"parameter": нельзя объявить аргументы по умолчанию для функций-членов управляемого типа, типа WinRT или универсальных функций

Запрещено объявлять параметр метода с аргументом по умолчанию. Перегруженные формы метода — один из способов решения этой проблемы. То есть вам нужно определить метод с тем же именем без параметров и затем инициализировать переменную в теле метода.

Следующий пример приводит к возникновению ошибки C3222:

```cpp
// C3222_2.cpp
// compile with: /clr
public ref class G {
   void f( int n = 0 );   // C3222
};
```
