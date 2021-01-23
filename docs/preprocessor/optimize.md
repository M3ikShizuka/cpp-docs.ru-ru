---
description: 'Дополнительные сведения: оптимизация pragma'
title: увеличить pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.optimize
- optimize_CPP
helpviewer_keywords:
- pragma, optimize
- optimize pragma
no-loc:
- pragma
ms.openlocfilehash: d9044788d0eea394867622d0f7aea1e365ad3399
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713458"
---
# <a name="optimize-no-locpragma"></a>`optimize` pragma

Задает оптимизацию для каждой функции по функциям.

## <a name="syntax"></a>Синтаксис

> **`#pragma optimize( "`** [ *Оптимизация-список* ] **`",`** { **`on`** | **`off`** } **`)`**

## <a name="remarks"></a>Примечания

**`optimize`** pragma Должен находиться за пределами функции. Он вступает в силу в первой функции, определенной после того, как pragma будет показана функция. **`on`** Аргументы и **`off`** включают параметры, заданные в *списке оптимизация —* on или OFF.

*Оптимизация-список* может быть равен нулю или большему числу параметров, приведенных в следующей таблице.

### <a name="parameters-of-the-optimize-pragma"></a>Параметры директивы #pragma optimize

| Параметры | Тип оптимизации |
|--------------------|--------------------------|
| **`g`** | Включить глобальную оптимизацию. |
| **`s`** или **`t`** | Указывать короткую или быструю последовательность машинного кода. |
| **`y`** | Создавать указатели фреймов в стеке программы. |

Эти параметры совпадают с буквами, используемыми в [`/O`](../build/reference/o-options-optimize-code.md) параметрах компилятора. Например, следующий пример pragma эквивалентен **`/Os`** параметру компилятора:

```cpp
#pragma optimize( "s", on )
```

Использование **`optimize`** pragma с пустой строкой ( **`""`** ) является особой формой директивы:

При использовании **`off`** параметра происходит включение всех оптимизаций,,, **`g`** **`s`** **`t`** и **`y`** .

При использовании **`on`** параметра он сбрасывает оптимизацию до тех, которые были указаны с помощью [`/O`](../build/reference/o-options-optimize-code.md) параметра компилятора.

```cpp
#pragma optimize( "", off )
/* unoptimized code section */
#pragma optimize( "", on )
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
