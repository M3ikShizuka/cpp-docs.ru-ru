---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4001'
title: Предупреждение компилятора (уровень 4) C4001
ms.date: 11/04/2016
f1_keywords:
- C4001
helpviewer_keywords:
- C4001
ms.assetid: 414a47fe-d597-425e-9374-6a569231dc0a
ms.openlocfilehash: c28c1391b120983d72dc6e5b7a96faa937ee2598
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97262221"
---
# <a name="compiler-warning-level-4-c4001"></a>Предупреждение компилятора (уровень 4) C4001

использовано нестандартное расширение "однострочный комментарий"

> [!NOTE]
> Это предупреждение удаляется в Visual Studio 2017 версии 15,5, так как однострочные комментарии являются стандартными в C99.

Однострочные комментарии являются стандартными в C++ и стандартом в C, начиная с C99.
В режиме ограниченной совместимости с ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) файлы C, содержащие однострочные комментарии, создают C4001 из-за использования нестандартного расширения. Поскольку однострочные комментарии являются стандартными в C++, файлы C, содержащие однострочные комментарии, не создают C4001 при компиляции с расширениями Майкрософт (/Ze).

## <a name="example"></a>Пример

Чтобы отключить предупреждение, раскомментируйте [#pragma warning (Disable: 4001)](../../preprocessor/warning.md).

```cpp
// C4001.cpp
// compile with: /W4 /Za /TC
// #pragma warning(disable:4001)
int main()
{
   // single-line comment in main
   // C4001
}
```
