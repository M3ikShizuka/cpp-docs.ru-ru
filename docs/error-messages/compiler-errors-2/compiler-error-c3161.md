---
description: 'Дополнительные сведения о: Ошибка компилятора C3161'
title: Ошибка компилятора C3161
ms.date: 11/04/2016
f1_keywords:
- C3161
helpviewer_keywords:
- C3161
ms.assetid: 1fe2be85-a343-487b-8476-bf9e257eb29d
ms.openlocfilehash: 4e45d64e1c1f318a126122148c2dd8e3ddb9c5af
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97203969"
---
# <a name="compiler-error-c3161"></a>Ошибка компилятора C3161

"Interface": недопустимый вложенный класс, структура, объединение или интерфейс в интерфейсе; Недопустимый вложенный интерфейс в классе, структуре или объединении

[__Interface](../../cpp/interface.md) может находиться только в глобальной области видимости или в пространстве имен. Класс, структура или объединение не могут присутствовать в интерфейсе.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3161.

```cpp
// C3161.cpp
// compile with: /c
__interface X {
   __interface Y {};   // C3161 A nested interface
};
```
