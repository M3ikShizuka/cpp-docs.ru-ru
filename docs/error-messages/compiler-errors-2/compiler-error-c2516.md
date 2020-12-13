---
description: 'Дополнительные сведения о: Ошибка компилятора C2516'
title: Ошибка компилятора C2516
ms.date: 11/04/2016
f1_keywords:
- C2516
helpviewer_keywords:
- C2516
ms.assetid: cd3accc1-0179-4a13-9587-616908c4ad1d
ms.openlocfilehash: 1561a6917d26a9cc4c71a8970e7a75512c1a1b61
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339292"
---
# <a name="compiler-error-c2516"></a>Ошибка компилятора C2516

"имя": не является допустимым базовым классом

Класс является производным от имени типа, определенного **`typedef`** инструкцией.

Следующий пример приводит к возникновению ошибки C2516:

```cpp
// C2516.cpp
typedef unsigned long ulong;
class C : public ulong {}; // C2516
```
