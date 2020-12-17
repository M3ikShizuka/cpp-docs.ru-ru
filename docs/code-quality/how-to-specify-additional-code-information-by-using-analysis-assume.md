---
description: Дополнительные сведения об указании дополнительных сведений о коде с помощью _Analysis_assume_.
title: Использование _Analysis_assume_ для указания анализа кода
ms.date: 12/16/2020
ms.topic: conceptual
f1_keywords:
- _Analysis_assume_
helpviewer_keywords:
- _Analysis_assume_
ms.openlocfilehash: f4244a896d4334cb6c5e857e63b39be0cd53b08b
ms.sourcegitcommit: 387ce22a3b0137f99cbb856a772b5a910c9eba99
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "97645128"
---
# <a name="how-to-specify-additional-code-information-by-using-_analysis_assume_"></a>Инструкции по указанию дополнительных сведений о коде с помощью `_Analysis_assume_`

Вы можете предоставить подсказки средству анализа кода для кода C/C++, который поможет анализировать процесс анализа и сократить число предупреждений. Чтобы предоставить дополнительные сведения, используйте следующий макрос функции:

`_Analysis_assume( expr )`

*`expr`* — любое выражение, для которого предполагается вычисление значения true.

Средство анализа кода предполагает, что условие, представленное выражением, *`expr`* имеет значение true в точке, где отображается функция. И он остается истинным до тех пор, пока не изменится, например, *`expr`* путем присваивания переменной.

> [!NOTE]
> `_Analysis_assume_` не влияет на оптимизацию кода. Вне средства анализа кода `_Analysis_assume_` определяется как отсутствие операций.

## <a name="example"></a>Пример

Следующий код используется `_Analysis_assume_` для исправления предупреждения анализа кода [C6388](../code-quality/c6388.md):

```cpp
#include <windows.h>
#include <codeanalysis\sourceannotations.h>

using namespace vc_attributes;

//requires pc to be null
void f([Pre(Null=Yes)] char* pc);

// calls free and sets ch to null
void FreeAndNull(char** ch);

void test()
{
    char pc = (char)malloc(5);
    FreeAndNull(&pc);
    _Analysis_assume_(pc == NULL);
    f(pc);
}
```

## <a name="see-also"></a>См. также раздел

- [__assume](../intrinsics/assume.md)
