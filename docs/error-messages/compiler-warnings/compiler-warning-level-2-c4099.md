---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 2) C4099'
title: Предупреждение компилятора (уровень 2) C4099
ms.date: 11/04/2016
f1_keywords:
- C4099
helpviewer_keywords:
- C4099
ms.assetid: 00bb803d-cae7-4ab8-8969-b46f54139ac8
ms.openlocfilehash: c35ce10560ca81f9457f6a21c4c55d96996e7645
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326521"
---
# <a name="compiler-warning-level-2-c4099"></a>Предупреждение компилятора (уровень 2) C4099

"идентификатор": имя типа сначала появлялось с помощью "objecttype1", которое теперь было показано с помощью "objecttype2"

Объект, объявленный как структура, определяется как класс, или объект, объявленный как класс, определяется как структура. Компилятор использует тип, заданный в определении.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4099.

```cpp
// C4099.cpp
// compile with: /W2 /c
struct A;
class A {};   // C4099, use different identifer or use same object type
```
