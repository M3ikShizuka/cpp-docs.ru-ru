---
description: 'Дополнительные сведения о: Ошибка компилятора C2348'
title: Ошибка компилятора C2348
ms.date: 11/04/2016
f1_keywords:
- C2348
helpviewer_keywords:
- C2348
ms.assetid: 4c4d701f-ccf1-46fe-9ddb-3f341684f269
ms.openlocfilehash: 829bd94c8fe78280b8b49b74f218e2143dda4335
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298361"
---
# <a name="compiler-error-c2348"></a>Ошибка компилятора C2348

"имя типа": не является статистическим выражением в стиле C, не может быть экспортировано во внедренный IDL

Чтобы поместить **`struct`** в IDL-файл с атрибутом [Export](../../windows/attributes/export.md) , параметр **`struct`** должен содержать только данные.

Следующий пример приводит к возникновению ошибки C2348:

```cpp
// C2348.cpp
// C2348 error expected
[ module(name="SimpleMidlTest") ];

[export]
struct Point {
   // Delete the following two lines to resolve.
   Point() : m_i(0), m_j(0) {}
   Point(int i, int j) : m_i(i), m_j(j) {}

   int m_i;
   int m_j;
};
```
