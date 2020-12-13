---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 2) C4309'
title: Предупреждение компилятора (уровень 2) C4309
ms.date: 11/04/2016
f1_keywords:
- C4309
helpviewer_keywords:
- C4309
ms.assetid: cb3f41ef-fd8a-4def-baa1-924e751fca68
ms.openlocfilehash: 8ae49967078f8569a7830c2a2e2ce61f9d25e20d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339178"
---
# <a name="compiler-warning-level-2-c4309"></a>Предупреждение компилятора (уровень 2) C4309

"преобразование": усечение постоянного значения

Преобразование типа приводит к тому, что константа превысит пространство, выделенное для него. Для константы может потребоваться использовать больший тип.

Следующий пример приводит к возникновению ошибки C4309:

```cpp
// C4309.cpp
// compile with: /W2
int main()
{
   char c = 128;   // C4309
}
```
