---
description: 'Дополнительные сведения о: Ошибка компилятора C3353'
title: Ошибка компилятора C3353
ms.date: 11/04/2016
f1_keywords:
- C3353
helpviewer_keywords:
- C3353
ms.assetid: 5699c04b-d504-46ce-bf71-c200318fed71
ms.openlocfilehash: 50ff7a6b104f3e16ce17f1398da49a146c0d41a4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335039"
---
# <a name="compiler-error-c3353"></a>Ошибка компилятора C3353

delegate: создание делегата допускается только из глобальной функции или функции-члена управляемого типа или типа WinRT

Делегаты, объявленные с ключевым словом [делегата](../../extensions/delegate-cpp-component-extensions.md) , могут быть объявлены только в глобальной области видимости.

Следующий пример приводит к возникновению ошибки C3353:

```cpp
// C3353.cpp
// compile with: /clr
delegate int f;   // C3353
```
