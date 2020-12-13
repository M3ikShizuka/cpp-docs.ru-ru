---
description: 'Дополнительные сведения о: Ошибка компилятора C2499'
title: Ошибка компилятора C2499
ms.date: 11/04/2016
f1_keywords:
- C2499
helpviewer_keywords:
- C2499
ms.assetid: b323ff4d-b3c1-4bfd-b052-ae7292d53222
ms.openlocfilehash: 35d6c0017792c14b99418166af7ae6a84745340d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335080"
---
# <a name="compiler-error-c2499"></a>Ошибка компилятора C2499

"класс": класс не может быть собственным базовым классом

Предпринята попытка указать класс, определяемый как базовый класс.

Следующий пример приводит к возникновению ошибки C2499:

```cpp
// C2499.cpp
// compile with: /c
class CMyClass : public CMyClass {};   // C2499
class CMyClass{};   // OK
```
