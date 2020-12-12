---
description: 'Дополнительные сведения о: Ошибка компилятора C3699'
title: Ошибка компилятора C3699
ms.date: 11/04/2016
f1_keywords:
- C3699
helpviewer_keywords:
- C3699
ms.assetid: 47c29afc-ab8b-4238-adfe-788dd6e00b3b
ms.openlocfilehash: 670b5c41aad9afcece8d8cd292727ad64925a4ab
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97228720"
---
# <a name="compiler-error-c3699"></a>Ошибка компилятора C3699

"оператор": невозможно использовать это косвенное обращение для типа "тип"

Предпринята попытка использовать косвенное обращение, которое не разрешено в `type` .

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C3699.

```cpp
// C3699.cpp
// compile with: /clr /c
using namespace System;
int main() {
   String * s;   // C3699
   // try the following line instead
   // String ^ s2;
}
```

Тривиальное свойство не может иметь ссылочный тип. Дополнительные сведения см. в разделе [property](../../extensions/property-cpp-component-extensions.md) . Следующий пример приводит к возникновению ошибки C3699.

```cpp
// C3699_b.cpp
// compile with: /clr /c
ref struct C {
   property System::String % x;   // C3699
   property System::String ^ y;   // OK
};
```

Эквивалентом синтаксиса "указатель на указатель" является обработчик для отслеживаемой ссылки. Следующий пример приводит к возникновению ошибки C3699.

```cpp
// C3699_c.cpp
// compile with: /clr /c
using namespace System;
void Test(String ^^ i);   // C3699
void Test2(String ^% i);
```
