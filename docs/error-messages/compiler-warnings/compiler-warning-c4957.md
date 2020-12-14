---
description: 'Дополнительные сведения о: предупреждение компилятора C4957'
title: Предупреждение компилятора C4957
ms.date: 11/04/2016
f1_keywords:
- C4957
helpviewer_keywords:
- C4957
ms.assetid: a18c52d4-23e2-44f1-b4b5-f7fa5a7f3987
ms.openlocfilehash: ac9d41b6161f658eb7debf438c495fbc57c6bb2e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314832"
---
# <a name="compiler-warning-c4957"></a>Предупреждение компилятора C4957

> "*приведение*": явное приведение "*cast_from*" к "*cast_to*" не поддается проверке

## <a name="remarks"></a>Комментарии

В результате приведения будет создан недоступный для проверки образ.

Некоторые приведения являются надежными (например, **`static_cast`** триггеры запускают пользовательские преобразования и **`const_cast`** ). При выполнении приведения [safe_cast](../../extensions/safe-cast-cpp-component-extensions.md) гарантированно создается проверяемый код.

Дополнительные сведения см. в разделе [чистый и проверяемый код (C++/CLI)](../../dotnet/pure-and-verifiable-code-cpp-cli.md).

Параметр компилятора **/clr: Сейф** является устаревшим в visual Studio 2015 и не поддерживается в visual Studio 2017.

Это предупреждение выдается в качестве ошибки, и его можно отключить с помощью прагмы [warning](../../preprocessor/warning.md) или параметра компилятора [/wd](../../build/reference/compiler-option-warning-level.md) .

## <a name="example"></a>Пример

Следующий пример приводит к возникновению предупреждения C4957:

```cpp
// C4957.cpp
// compile with: /clr:safe
// #pragma warning( disable : 4957 )
using namespace System;
int main() {
   Object ^ o = "Hello, World!";
   String ^ s = static_cast<String^>(o);   // C4957
   String ^ s2 = safe_cast<String^>(o);   // OK
}
```
