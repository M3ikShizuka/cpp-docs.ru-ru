---
description: 'Дополнительные сведения о: Ошибка компилятора C2150'
title: Ошибка компилятора C2150
ms.date: 11/04/2016
f1_keywords:
- C2150
helpviewer_keywords:
- C2150
ms.assetid: 21e82a10-c1d4-4c0d-9dc6-c5d92ea42a31
ms.openlocfilehash: 5a609edba74e2aee8e0d2a6275fa1ca40fafe5c6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97223520"
---
# <a name="compiler-error-c2150"></a>Ошибка компилятора C2150

> "*идентификатор*": битовое поле должно иметь тип "int", "знаковое целое число" или "Неподписанное целое число"

Базовый тип для битового поля должен быть **`int`** , **`signed int`** или **`unsigned int`** .

## <a name="example"></a>Пример

В этом примере показано, как можно столкнуться с C2150, и как это можно исправить:

```cpp
// C2150.cpp
// compile with: /c
struct A {
   float a : 8;    // C2150
   int i : 8;      // OK
};
```
