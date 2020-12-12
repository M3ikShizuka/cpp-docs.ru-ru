---
description: 'Дополнительные сведения о: Ошибка компилятора C2286'
title: Ошибка компилятора C2286
ms.date: 11/04/2016
f1_keywords:
- C2286
helpviewer_keywords:
- C2286
ms.assetid: 078e0201-35cc-42e2-8dbc-6f8cf557b098
ms.openlocfilehash: 89c8b69c42188d448fad0cd08287773d7a713d08
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298465"
---
# <a name="compiler-error-c2286"></a>Ошибка компилятора C2286

указатели на члены представления "идентификатор" уже заданы как "наследование" — объявление игнорируется

Для класса существует два различных представления указателей на члены.

Дополнительные сведения см. в разделе [Ключевые слова наследования](../../cpp/inheritance-keywords.md).

## <a name="example"></a>Пример

При компиляции следующего примера возникнет ошибка C2286:

```cpp
// C2286.cpp
// compile with: /c
class __single_inheritance X;
class __multiple_inheritance X;   // C2286
class  __multiple_inheritance Y;   // OK
```
