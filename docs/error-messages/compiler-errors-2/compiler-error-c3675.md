---
description: 'Дополнительные сведения о: Ошибка компилятора C3675'
title: Ошибка компилятора C3675
ms.date: 11/04/2016
f1_keywords:
- C3675
helpviewer_keywords:
- C3675
ms.assetid: 87461613-6633-430b-b95d-c7cb1bb63776
ms.openlocfilehash: 0e8ea8d3450cd7a145e596f7122a5d2cbb31c5fd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97228746"
---
# <a name="compiler-error-c3675"></a>Ошибка компилятора C3675

"функция": зарезервировано, так как определено "свойство"

При объявлении простого свойства компилятор создает методы доступа get и Set, и эти имена находятся в области программы.  Создаваемые компилятором имена формируются с помощью предустановленного get_ и set_ к имени свойства.  Поэтому нельзя объявлять функции с тем же именем, что и методы доступа, создаваемые компилятором.

Дополнительные сведения см. в разделе [property](../../extensions/property-cpp-component-extensions.md) .

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3675.

```cpp
// C3675.cpp
// compile with: /clr /c
ref struct C {
public:
   property int Size;
   int get_Size() { return 0; }   // C3675
};
```
