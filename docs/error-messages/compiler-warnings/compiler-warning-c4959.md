---
description: 'Дополнительные сведения о: предупреждение компилятора C4959'
title: Предупреждение компилятора C4959
ms.date: 11/04/2016
f1_keywords:
- C4959
helpviewer_keywords:
- C4959
ms.assetid: 3a128f3e-4d8a-4565-ba1a-5d32fdeb5982
ms.openlocfilehash: 3a4fae04ee654caf23776a7bf4d6b073853bd03a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336082"
---
# <a name="compiler-warning-c4959"></a>Предупреждение компилятора C4959

> не удается определить неуправляемую структуру "*тип*" в/CLR: Сейф, так как доступ к ее членам дает непроверяемый код

## <a name="remarks"></a>Комментарии

Обращение к члену неуправляемого типа приводит к формированию непроверяемого (peverify.exe) образа.

Дополнительные сведения см. в разделе [чистый и проверяемый код (C++/CLI)](../../dotnet/pure-and-verifiable-code-cpp-cli.md).

Параметр компилятора **/clr: Сейф** является устаревшим в visual Studio 2015 и не поддерживается в visual Studio 2017.

Это предупреждение выдается в качестве ошибки, и его можно отключить с помощью прагмы [warning](../../preprocessor/warning.md) или параметра компилятора [/wd](../../build/reference/compiler-option-warning-level.md) .

## <a name="example"></a>Пример

Следующий пример приводит к возникновению предупреждения C4959:

```cpp
// C4959.cpp
// compile with: /clr:safe

// Uncomment the following line to resolve.
// #pragma warning( disable : 4959 )
struct X {
   int data;
};

int main() {
   X x;
   x.data = 10;   // C4959
}
```
