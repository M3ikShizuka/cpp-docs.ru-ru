---
description: 'Дополнительные сведения о: Ошибка компилятора C3101'
title: Ошибка компилятора C3101
ms.date: 11/04/2016
f1_keywords:
- C3101
helpviewer_keywords:
- C3101
ms.assetid: 4f673766-d4f7-4632-94a5-d36a83f7f4b5
ms.openlocfilehash: e0c52eadd2af4b090b34f851d561535f360a7e59
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97116175"
---
# <a name="compiler-error-c3101"></a>Ошибка компилятора C3101

Недопустимое выражение для именованного аргумента атрибута "поле"

При инициализации аргумента именованного атрибута значение должно быть константой времени компиляции.

Дополнительные сведения об атрибутах см. в разделе [определяемые пользователем атрибуты](../../extensions/user-defined-attributes-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3101.

```cpp
// C3101.cpp
// compile with: /clr /c
ref class AAttribute : System::Attribute {
public:
   int Field;
};

extern int i;

[assembly:A(Field = i)];   // C3101
[assembly:A(Field = 0)];   // OK
```
