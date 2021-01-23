---
description: Дополнительные сведения об pragma директиве check_stack в Microsoft C/C++
title: check_stack pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.check_stack
- check_stack_CPP
helpviewer_keywords:
- check_stack pragma
- pragma, check_stack
- pragma, check_stack usage table
no-loc:
- pragma
ms.openlocfilehash: a395471625fed60fcf750ebac8f3159a89ba1487
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713718"
---
# <a name="check_stack-no-locpragma"></a>`check_stack` pragma

Предписывает компилятору отключить проверки стека **`off`** **`-`** , если задано значение (или), или включить проверку стека, если **`on`** задано значение (или **`+`** ).

## <a name="syntax"></a>Синтаксис

> **`#pragma check_stack(`** [{ **`on`** | **`off`** }] **`)`**\
> **`#pragma check_stack`** { **`+`** | **`-`** }

## <a name="remarks"></a>Примечания

Это pragma вступает в силу в первой функции, определенной после того, как pragma будет показана функция. Стековые зонды не являются частью макросов или функций, создаваемых как встроенные.

Если не предоставить аргумент для **`check_stack`** pragma , проверка стека вернется к поведению, указанному в командной строке. Дополнительные сведения см. в разделе [Параметры компилятора](../build/reference/compiler-options.md). `#pragma check_stack` [`/Gs`](../build/reference/gs-control-stack-checking-calls.md) В следующей таблице представлены сведения о взаимодействии с параметром и.

### <a name="using-the-check_stack-pragma"></a>Использование директивы #pragma check_stack

| Синтаксис | Скомпилировано с использованием<br /><br /> `/Gs` функцию? | Действие |
|--|--|--|
| `#pragma check_stack( )` или<br /><br /> `#pragma check_stack` | Да | Отключает проверку стека для последующих функций |
| `#pragma check_stack( )` или<br /><br /> `#pragma check_stack` | Нет | Включает проверку стека для последующих функций |
| `#pragma check_stack(on)`<br /><br /> или `#pragma check_stack +` | "Да" или "Нет". | Включает проверку стека для последующих функций |
| `#pragma check_stack(off)`<br /><br /> или `#pragma check_stack -` | "Да" или "Нет". | Отключает проверку стека для последующих функций |

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
