---
description: 'Дополнительные сведения о: Ошибка компилятора C3809'
title: Ошибка компилятора C3809
ms.date: 11/04/2016
f1_keywords:
- C3809
helpviewer_keywords:
- C3809
ms.assetid: 37eca584-c20c-464e-8e45-a987214b7ce4
ms.openlocfilehash: 62e7ff06e6ed5bf34861fdbae3f823e19ad5aad4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97328202"
---
# <a name="compiler-error-c3809"></a>Ошибка компилятора C3809

class: управляемый тип или тип WinRT не может иметь дружественные функции, классы и интерфейсы

Управляемые типы и типы среды выполнения Windows не могут иметь дружественные элементы. Чтобы устранить эту ошибку, не объявляйте дружественные элементы внутри управляемых или типов среды выполнения Windows.

Следующий пример приводит к возникновению ошибки C3809:

```cpp
// C3809a.cpp
// compile with: /clr
ref class A {};

ref class B
{
public:
   friend ref class A;   // C3809
};

int main()
{
}
```
