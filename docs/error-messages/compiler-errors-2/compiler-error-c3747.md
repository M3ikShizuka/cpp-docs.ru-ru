---
description: 'Дополнительные сведения о: Ошибка компилятора C3747'
title: Ошибка компилятора C3747
ms.date: 11/04/2016
f1_keywords:
- C3747
helpviewer_keywords:
- C3747
ms.assetid: a9a4be67-5d9c-4dcc-9ae9-baae46cbecde
ms.openlocfilehash: 9e40b887d5a107eed5e93a7f3827ba4e8c1590e4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340207"
---
# <a name="compiler-error-c3747"></a>Ошибка компилятора C3747

отсутствует параметр типа по умолчанию: параметр param

Значения универсальных шаблонов или параметров шаблона со значениями по умолчанию не могут содержаться в списке параметров параметрами, не имеющими значений по умолчанию.

Следующий пример приводит к возникновению ошибки C3747:

```cpp
// C3747.cpp
template <class T1 = int, class T2>   // C3747
struct MyStruct {};
```

Возможное решение:

```cpp
// C3747b.cpp
// compile with: /c
template <class T1, class T2 = int>
struct MyStruct {};
```
