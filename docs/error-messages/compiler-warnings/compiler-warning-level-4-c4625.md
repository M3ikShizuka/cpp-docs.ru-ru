---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4625'
title: Предупреждение компилятора (уровень 4) C4625
ms.date: 11/04/2016
f1_keywords:
- C4625
helpviewer_keywords:
- C4625
ms.assetid: 4cc99e50-846c-4784-97da-48b977067851
ms.openlocfilehash: 1b154e1f2e52c21affd47c1b0fc30d29b290269e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134229"
---
# <a name="compiler-warning-level-4-c4625"></a>Предупреждение компилятора (уровень 4) C4625

"производный класс": не удалось создать конструктор копии, так как конструктор копии для базового класса недоступен или удален

Конструктор копирования был удален или недоступен для базового класса, поэтому он не был создан для производного класса. Любая попытка создать объект этого типа приведет к ошибке компилятора.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

## <a name="example"></a>Пример

В следующем примере показано возникновение ошибки C4625 и приводятся сведения по ее устранению.

```cpp
// C4625.cpp
// compile with: /W4 /c
#pragma warning(default : 4625)

struct A {
   A() {}

private:
   A(const A&) {}
};

struct C : private virtual A {};
struct B :  C {};   // C4625 no copy constructor

struct D : A {};
struct E :  D {};   // OK
```
