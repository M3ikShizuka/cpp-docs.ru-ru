---
description: 'Дополнительные сведения о: Ошибка компилятора C2842'
title: Ошибка компилятора C2842
ms.date: 11/04/2016
f1_keywords:
- C2842
helpviewer_keywords:
- C2842
ms.assetid: 8674f08d-9f50-46ad-9229-abc6b74fa0e5
ms.openlocfilehash: f086c6c5fcfa451f320d96470615e4f5f4d5674a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97119987"
---
# <a name="compiler-error-c2842"></a>Ошибка компилятора C2842

> "*класс*": тип управляемого или WinRT не может определять собственный оператор "operator new" или "operator delete"

## <a name="remarks"></a>Комментарии

Для управления выделением памяти в собственной куче можно определить собственный **оператор New** или **оператор DELETE** . Однако эти операторы не могут быть определены в ссылочных классах , так как только они выделяются в управляемой куче.

Дополнительные сведения см. в разделе [определяемые пользователем операторы (C++/CLI)](../../dotnet/user-defined-operators-cpp-cli.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2842:

```cpp
// C2842.cpp
// compile with: /clr /c
ref class G {
   void* operator new( size_t nSize );   // C2842
};
```
