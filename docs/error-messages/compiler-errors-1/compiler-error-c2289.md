---
description: 'Дополнительные сведения о: Ошибка компилятора C2289'
title: Ошибка компилятора C2289
ms.date: 11/04/2016
f1_keywords:
- C2289
helpviewer_keywords:
- C2289
ms.assetid: cb41a29e-1b06-47dc-bfce-8d73bd63a0df
ms.openlocfilehash: ba9af908af6defaccd6825ce3dad412ad6914c77
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185964"
---
# <a name="compiler-error-c2289"></a>Ошибка компилятора C2289

Множественное использование одного и того же квалификатора типа

Объявление типа или определение использует квалификатор типа ( **`const`** , **`volatile`** , **`signed`** или **`unsigned`** ) более одного раза, что приводит к ошибке при совместимости с ANSI (**/Za**).

При компиляции следующего примера возникнет ошибка C2286:

```cpp
// C2289.cpp
// compile with: /Za /c
volatile volatile int i;   // C2289
volatile int j;   // OK
```
