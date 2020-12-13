---
description: 'Дополнительные сведения о: Ошибка компилятора C2993'
title: Ошибка компилятора C2993
ms.date: 11/04/2016
f1_keywords:
- C2993
helpviewer_keywords:
- C2993
ms.assetid: 4ffd2b78-654b-46aa-95a6-b62101cf91c8
ms.openlocfilehash: 2c43d4f3e54378d419f1945b1f6b38e9ee4d9758
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97136426"
---
# <a name="compiler-error-c2993"></a>Ошибка компилятора C2993

"идентификатор": недопустимый тип для параметра шаблона "параметр", не являющегося типом

Нельзя объявить шаблон с аргументом Structure или Union. Используйте указатели для передачи структур и объединений в качестве параметров шаблона.

Следующий пример приводит к возникновению ошибки C2993:

```cpp
// C2993.cpp
// compile with: /c
// C2993 expected
struct MyStruct {
   int a;char b;
};

template <class T, struct MyStruct S>   // C2993

// try the following line instead
// template <class T, struct MyStruct * S>
class CMyClass {};
```

Эта ошибка также будет сформирована в результате работы по согласованности компилятора, выполненной в Visual Studio .NET 2003: параметры шаблона с плавающей запятой, не являющиеся типами, больше не допускаются. Стандарт C++ не допускает параметры шаблона с плавающей запятой, не являющиеся типами.

Если это шаблон функции, используйте аргумент функции для передачи параметра шаблона, не являющегося типом с плавающей запятой (этот код будет допустимым в версиях Visual Studio .NET 2003 и Visual Studio .NET Visual C++). Если это шаблон класса, простого решения не существует.

```cpp
// C2993b.cpp
// compile with: /c
template<class T, float f> void func(T) {}   // C2993

// OK
template<class T>   void func2(T, float) {}
```
