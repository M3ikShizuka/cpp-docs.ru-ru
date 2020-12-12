---
description: 'Дополнительные сведения о: Ошибка компилятора C3179'
title: Ошибка компилятора C3179
ms.date: 11/04/2016
f1_keywords:
- C3179
helpviewer_keywords:
- C3179
ms.assetid: 60d7e41b-25fd-48ac-8b79-830c062f4dcd
ms.openlocfilehash: 5f4b573c822eff68d972517f9fac093071cf2a0c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174160"
---
# <a name="compiler-error-c3179"></a>Ошибка компилятора C3179

неименованный управляемый тип или тип WinRT не допускается

Все классы и структуры среды CLR и WinRT должны иметь имена.

В следующем примере показано возникновение ошибки C3179 и приводятся сведения по ее устранению.

```cpp
// C3179a.cpp
// compile with: /clr /c
typedef value struct { // C3179
// try the following line instead
// typedef value struct MyStruct {
   int i;
} V;
```
