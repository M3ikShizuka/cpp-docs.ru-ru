---
description: Дополнительные сведения об pragma директиве inline_depth в Microsoft C/C++
title: inline_depth pragma
ms.date: 01/22/2021
f1_keywords:
- inline_depth_CPP
- vc-pragma.inline_depth
helpviewer_keywords:
- pragma, inline_depth
- inline_depth pragma
no-loc:
- pragma
ms.openlocfilehash: 6daffdbcb598304925675c15c955941eb8369d23
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713575"
---
# <a name="inline_depth-no-locpragma"></a>`inline_depth` pragma

Задает глубину встроенного эвристического поиска. Функции с глубиной в графе вызовов больше указанного значения не являются встроенными.

## <a name="syntax"></a>Синтаксис

> **`#pragma inline_depth(`** [ *n* ] **`)`**

## <a name="remarks"></a>Примечания

Это pragma контролирует встраивание функций, помеченных [`inline`](../cpp/inline-functions-cpp.md) и [`__inline`](../cpp/inline-functions-cpp.md) , или встроенных автоматически, в **`/Ob`** параметре компилятора. Дополнительные сведения см. в разделе [ `/Ob` (расширение встроенных функций)](../build/reference/ob-inline-function-expansion.md).

значение *n* может быть в диапазоне от 0 до 255, где 255 означает неограниченную глубину в графе вызовов. Значение 0 препятствует встроенному расширению. Если *n* не указано, используется значение по умолчанию 254.

**`inline_depth`** pragma Определяет, сколько раз можно раскрыть ряд вызовов функций. Например, предположим, что встроенная глубина равна 4. Если вызов B, а затем B вызывает C, все три вызова разворачиваются встроенными. Однако, если ближайшее расширение глубины равно 2, разворачиваются только A и B, а C остается в виде вызова функции.

Чтобы использовать этот pragma параметр, необходимо задать **`/Ob`** для параметра компилятора значение 1 или выше. Глубина, заданная с помощью этого параметра, pragma вступает в силу при первом вызове функции после pragma .

Встроенную глубину можно уменьшить во время расширения, но не увеличивать. Если встроенная глубина равна 6, а во время расширения препроцессор встречает значение, равное **`inline_depth`** pragma 8, глубина остается 6.

Параметр **`inline_depth`** pragma не влияет на функции, помеченные как **`__forceinline`** .

> [!NOTE]
> Подстановка для рекурсивных функций выполняется на глубину не более 16 вызовов.

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)\
[`inline_recursion`](../preprocessor/inline-recursion.md)
