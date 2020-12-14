---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4382'
title: Предупреждение компилятора (уровень 1) C4382
ms.date: 11/04/2016
f1_keywords:
- C4382
helpviewer_keywords:
- C4382
ms.assetid: 34be9ad3-bae6-411a-8f80-0c8fd0d2c092
ms.openlocfilehash: 038225aea9592070b44af138be9deb5076e2f5f7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97311309"
---
# <a name="compiler-warning-level-1-c4382"></a>Предупреждение компилятора (уровень 1) C4382

> Создание "*типа*": тип с деструктором __clrcall или конструктором копии может быть перехвачен только в модуле/CLR: pure

## <a name="remarks"></a>Комментарии

Параметр компилятора **/clr: pure** является устаревшим в visual Studio 2015 и не поддерживается в visual Studio 2017.

При компиляции с параметром **/CLR** (не **/clr: pure**) обработка исключений ждет, что функции-члены в собственном типе будут [__cdecl](../../cpp/cdecl.md) , а не [__clrcall](../../cpp/clrcall.md). Собственные типы с функциями-членами с использованием `__clrcall` соглашения о вызовах не могут быть перехвачены в модуле, скомпилированном с **параметром/CLR**.

Если исключение будет перехвачено в модуле, скомпилированном с **параметром/clr: pure**, это предупреждение можно игнорировать.

Дополнительные сведения см. в разделе [/CLR (компиляция среды CLR)](../../build/reference/clr-common-language-runtime-compilation.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4382.

```cpp
// C4382.cpp
// compile with: /clr /W1 /c
struct S {
   __clrcall ~S() {}
};

struct T {
   ~T() {}
};

int main() {
   S s;
   throw s;   // C4382

   S * ps = &s;
   throw ps;   // OK

   T t;
   throw t;   // OK
}
```
