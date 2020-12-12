---
description: 'Дополнительные сведения о: Ошибка компилятора C2021'
title: Ошибка компилятора C2021
ms.date: 11/04/2016
f1_keywords:
- C2021
helpviewer_keywords:
- C2021
ms.assetid: 064f32e2-3794-48d5-9767-991003dcb36a
ms.openlocfilehash: 823d9c3d42f1df7bc6f6f398dafd804daef76110
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175642"
---
# <a name="compiler-error-c2021"></a>Ошибка компилятора C2021

требуется экспоненциальное значение, а не "символ"

Символ, используемый в качестве экспоненты константы с плавающей запятой, не является допустимым числом. Обязательно используйте показатель степени в диапазоне.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C2021:

```cpp
// C2021.cpp
float test1=1.175494351E;   // C2021
```

Возможное решение:

```cpp
// C2021b.cpp
// compile with: /c
float test2=1.175494351E8;
```
