---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4964'
title: Предупреждение компилятора (уровень 1) C4964
ms.date: 11/04/2016
f1_keywords:
- C4964
helpviewer_keywords:
- C4964
ms.assetid: b89c9274-8a92-4b7c-aa30-3fbb1b68ac73
ms.openlocfilehash: 102c04332bd40f6f1ae95cbd025c7400fc77dbf4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327924"
---
# <a name="compiler-warning-level-1-c4964"></a>Предупреждение компилятора (уровень 1) C4964

Параметры оптимизации не указаны. сведения о профиле не будут собраны

Указаны [/GL](../../build/reference/gl-whole-program-optimization.md) и [/LTCG](../../build/reference/ltcg-link-time-code-generation.md) , но не было запрошено ни одной оптимизации, поэтому PGC-файлы не будут созданы и, следовательно, оптимизация профиля не будет возможна.

Если вы хотите, чтобы файлы. PGC создавались при запуске приложения, укажите один из параметров компилятора [/o](../../build/reference/o-options-optimize-code.md) .

Следующий пример приводит к возникновению ошибки C4964:

```cpp
// C4964.cpp
// compile with: /W1 /GL /link /ltcg:pgi
// C4964 expected
// Add /O2, for example, to the command line to resolve this warning.
int main() {
   int i;
}
```
