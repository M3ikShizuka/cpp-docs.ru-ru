---
description: 'Дополнительные сведения о: Ошибка компилятора C2825'
title: Ошибка компилятора C2825
ms.date: 11/04/2016
f1_keywords:
- C2825
helpviewer_keywords:
- C2825
ms.assetid: c832f1c1-5184-4fc2-9356-12b21daa7af3
ms.openlocfilehash: fa72f915a77ec26e6da402ae8ff87ee380f1838c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194583"
---
# <a name="compiler-error-c2825"></a>Ошибка компилятора C2825

var: должен быть классом или пространством имен, если за ним следует "::"

Выполнена неудачная попытка формирования полного имени.

Например, убедитесь, что код не содержит объявление функции, где имя функции начинается с::.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2825:

```cpp
// C2825.cpp
typedef int i;
int main() {
   int* p = new int;
   p->i::i();   // C2825
   // try the following line instead
   // p->i::~i();
}
```
