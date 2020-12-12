---
description: 'Дополнительные сведения о: Ошибка компилятора C2951'
title: Ошибка компилятора C2951
ms.date: 11/04/2016
f1_keywords:
- C2951
helpviewer_keywords:
- C2951
ms.assetid: c6f95aa2-c894-425b-a51c-d40d70c8daa1
ms.openlocfilehash: 7f3030764cdd36d40fbd78a8c3768c7dc1085c21
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97322111"
---
# <a name="compiler-error-c2951"></a>Ошибка компилятора C2951

объявления типов разрешены только в глобальной области видимости, в пространстве имен или на уровне класса

Нельзя объявить универсальный класс или класса шаблона за пределами области глобальных или пространств имен. При внесении универсальных или шаблонных объявлений в включаемый файл убедитесь, что включаемый файл находится в глобальной области видимости.

Следующий пример приводит к возникновению ошибки C2951:

```cpp
// C2951.cpp
template <class T>
class A {};

int main() {
   template <class T>   // C2951
   class B {};
}
```

C2951 также может возникать при использовании универсальных шаблонов:

```cpp
// C2951b.cpp
// compile with: /clr /c

// OK
generic <class T>
ref class GC { };

int main() {
   generic <class T> ref class GC2 {};   // C2951
}
```
