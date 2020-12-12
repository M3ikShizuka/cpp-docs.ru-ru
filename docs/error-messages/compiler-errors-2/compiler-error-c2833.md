---
description: 'Дополнительные сведения о: Ошибка компилятора C2833'
title: Ошибка компилятора C2833
ms.date: 11/04/2016
f1_keywords:
- C2833
helpviewer_keywords:
- C2833
ms.assetid: b9418ce1-e2ee-4599-8959-6fde89c27569
ms.openlocfilehash: 3c1bd2cc60478dc5868c74d4bfeac1d7d3a4d9a1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194492"
---
# <a name="compiler-error-c2833"></a>Ошибка компилятора C2833

> оператор "operator *-Name*" не является распознаваемым оператором или типом

После слова **`operator`** должно следовать *имя оператора* , которое требуется переопределить, или тип, который требуется преобразовать.

Список операторов, которые можно определить в управляемом типе, см. в разделе [определяемые пользователем операторы](../../dotnet/user-defined-operators-cpp-cli.md).

Следующий пример приводит к возникновению ошибки C2833:

```cpp
// C2833.cpp
// compile with: /c
class A {};

void operator ::* ();   // C2833
void operator :: ();   // OK
```
