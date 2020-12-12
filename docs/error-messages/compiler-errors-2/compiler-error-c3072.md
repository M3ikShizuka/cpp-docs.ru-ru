---
description: 'Дополнительные сведения о: Ошибка компилятора C3072'
title: Ошибка компилятора C3072
ms.date: 11/04/2016
f1_keywords:
- C3072
helpviewer_keywords:
- C3072
ms.assetid: cdd5cb6b-c478-4698-adfa-c40188d34a18
ms.openlocfilehash: 02876a6983a47ce76f6e089bafde68af41034131
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320283"
---
# <a name="compiler-error-c3072"></a>Ошибка компилятора C3072

> оператор "*operator-Name*" не может применяться к экземпляру класса ссылки

для преобразования экземпляра ссылочного класса в тип Handle используется унарный оператор *Name-operator*

Для типа CLR требуются операторы CLR, а не машинные (или стандартные) операторы.  Дополнительные сведения см. в разделе [Отслеживание ссылочного оператора](../../extensions/tracking-reference-operator-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3072.

```cpp
// C3072.cpp
// compile with: /clr
ref class R {};

int main() {
   R r1;
   R^ r2 = &r1;   // C3072
   R^ r3 = %r1;   // OK
}
```
