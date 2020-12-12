---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4661'
title: Предупреждение компилятора (уровень 1) C4661
ms.date: 11/04/2016
f1_keywords:
- C4661
helpviewer_keywords:
- C4661
ms.assetid: 603bb8b7-356d-4eef-924b-64d769bac5bd
ms.openlocfilehash: 401f9a7229b4eec1f6484c49b6d2b1a18d8c49f8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318836"
---
# <a name="compiler-warning-level-1-c4661"></a>Предупреждение компилятора (уровень 1) C4661

"идентификатор": не указано подходящее определение для запроса явного создания экземпляра шаблона

Член класса шаблона не определен.

## <a name="example"></a>Пример

```cpp
// C4661.cpp
// compile with: /W1 /LD
template<class T> class MyClass {
public:
   void i();   // declaration but not definition
};
template MyClass< int >;  // C4661
```
