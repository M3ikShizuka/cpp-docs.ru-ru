---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4744'
title: Предупреждение компилятора (уровень 1) C4744
ms.date: 11/04/2016
f1_keywords:
- C4744
helpviewer_keywords:
- C4744
ms.assetid: f2a7d0b5-afd5-4926-abc3-cfbd367e3ff5
ms.openlocfilehash: d7be7c44d0e5abb1d0e3618ffa6ed1778a6410c7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97228460"
---
# <a name="compiler-warning-level-1-c4744"></a>Предупреждение компилятора (уровень 1) C4744

"var" имеет другой тип в "file1" и "File2": "тип1" и "тип2"

Внешняя переменная, упоминаемая или определенная в двух файлах, имеет разные типы в этих файлах.  Чтобы устранить эту проблему, либо сделайте определения типов одинаковыми, либо измените имя переменной в одном из файлов.

C4744 создается только при компиляции файлов с помощью параметра/GL.  Дополнительные сведения см. в разделе [/GL (оптимизация всей программы)](../../build/reference/gl-whole-program-optimization.md).

> [!NOTE]
> C4744 обычно происходит в файлах C (а не C++), так как в C++ имя переменной дополнено информацией о типе.  Когда пример (ниже) компилируется как C++, вы получите ошибку компоновщика LNK2019.

## <a name="examples"></a>Примеры

Этот образец содержит первое определение.

```c
// C4744.c
// compile with: /c /GL
int global;
```

Следующий пример приводит к возникновению ошибки C4744.

```c
// C4744b.c
// compile with: C4744.c /GL /W1
// C4744 expected
#include <stdio.h>

extern unsigned global;

main()
{
    printf_s("%d\n", global);
}
```
