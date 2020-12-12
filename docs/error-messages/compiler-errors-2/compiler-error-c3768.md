---
description: 'Дополнительные сведения о: Ошибка компилятора C3768'
title: Ошибка компилятора C3768
ms.date: 11/04/2016
f1_keywords:
- C3768
helpviewer_keywords:
- C3768
ms.assetid: 091f0d53-1dff-43fd-813d-5c43c85b6ab0
ms.openlocfilehash: 3203fe74fb1da91f24312f76ca11ac49711da8f9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97291718"
---
# <a name="compiler-error-c3768"></a>Ошибка компилятора C3768

> невозможно получить адрес виртуальной функции vararg в чистом управляемом коде

## <a name="remarks"></a>Комментарии

Параметр компилятора **/clr: pure** является устаревшим в visual Studio 2015 и не поддерживается в visual Studio 2017.

При компиляции с **параметром/clr: pure** невозможно получить адрес виртуальной `vararg` функции.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3768:

```cpp
// C3768.cpp
// compile with: /clr:pure
struct A
{
   virtual void f(...);
};

int main()
{
   &(A::f);   // C3768
}
```
