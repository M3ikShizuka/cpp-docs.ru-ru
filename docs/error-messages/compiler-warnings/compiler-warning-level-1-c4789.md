---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4789'
title: Предупреждение компилятора (уровень 1) C4789
ms.date: 03/25/2019
f1_keywords:
- C4789
helpviewer_keywords:
- C4789
ms.assetid: 5800c301-5afb-4af0-85c1-ceb54d775234
ms.openlocfilehash: c08264b1790788c2eaba7857f473a5bff42a2da3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334961"
---
# <a name="compiler-warning-level-1-c4789"></a>Предупреждение компилятора (уровень 1) C4789

> буфер "*идентификатор*" размером *N* байт будет переполнен; *M* байты будут записаны начиная со смещения *L*

## <a name="remarks"></a>Комментарии

**C4789** предупреждает о переполнении буфера при использовании конкретных функций среды выполнения C (CRT). Он также может сообщать о несоответствиях размеров при передаче параметров или при назначении. Предупреждение может возникнуть, если размеры данных известны во время компиляции. Это предупреждение предназначено для ситуаций, в которых типичные несоответствия размеров данных могут остаться незамеченными.

**C4789** предупреждает, когда данные копируются в блок данных, который, как известно, слишком мал во время компиляции.

Предупреждение возникает, если в копии используется встроенная форма одной из следующих функций CRT:

- [strcpy](../../c-runtime-library/reference/strcpy-wcscpy-mbscpy.md)

- [memset](../../c-runtime-library/reference/memset-wmemset.md)

- [memcpy](../../c-runtime-library/reference/memcpy-wmemcpy.md), [wmemcpy](../../c-runtime-library/reference/memcpy-wmemcpy.md)

Предупреждение также появляется при приведении параметра к более крупному типу данных, а затем для назначения копирования из ссылки lvalue.

Visual C++ может создать это предупреждение для пути кода, который никогда не выполнялся. Предупреждение можно временно отключить с помощью `#pragma`, как показано в следующем примере:

```cpp
#pragma warning( push )
#pragma warning( disable : 4789 )
// unused code that generates compiler warning C4789`
#pragma warning( pop )
```

Эта идиома позволяет Visual C++ создавать предупреждение для конкретного блока кода. `#pragma warning(push)` сохраняет существующее состояние перед тем, как `#pragma warning(disable: 4789)` изменяет его. `#pragma warning(pop)` восстанавливает отмененное состояние и устраняет последствия `#pragma warning(disable:4789)`. Дополнительные сведения о директиве препроцессора C++ `#pragma` см. в разделе директивы [warning](../../preprocessor/warning.md) и [pragma и ключевое слово __pragma](../../preprocessor/pragma-directives-and-the-pragma-keyword.md).

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C4789.

```cpp
// C4789.cpp
// compile with: /Oi /W1 /c
#include <string.h>
#include <stdio.h>

int main()
{
    char a[20];
    strcpy(a, "0000000000000000000000000\n");   // C4789

    char buf2[20];
    memset(buf2, 'a', 21);   // C4789

    char c;
    wchar_t w = 0;
    memcpy(&c, &w, sizeof(wchar_t));
}
```

Следующий пример приводит к возникновению ошибки C4789.

```cpp
// C4789b.cpp
// compile with: /W1 /O2 /c
// processor: x86
short G;

int main()
{
   int * p = (int *)&G;
   *p = 3;   // C4789 - writes an int through a pointer to short
}
```
