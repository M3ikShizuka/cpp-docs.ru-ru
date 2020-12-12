---
description: 'Дополнительные сведения о: Ошибка компилятора C2665'
title: Ошибка компилятора C2665
ms.date: 11/04/2016
f1_keywords:
- C2665
helpviewer_keywords:
- C2665
ms.assetid: a7f99b61-2eae-4f2b-ba75-ea68fd1e8312
ms.openlocfilehash: 784fe5ef0f24cd9e5fba99465d46f378b2b517fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97210807"
---
# <a name="compiler-error-c2665"></a>Ошибка компилятора C2665

"функция": ни одно из перегрузок number1 не может преобразовать параметр number2 из типа "тип"

Параметр перегруженной функции не может быть преобразован в требуемый тип.  Возможные решения:

- Укажите оператор преобразования.

- Используйте явное преобразование.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2665.

```cpp
// C2665.cpp
void func(short, char*){}
void func(char*, char*){}

int main() {
   func(0, 1);   // C2665
   func((short)0, (char*)1);   // OK
}
```
