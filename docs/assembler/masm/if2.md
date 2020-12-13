---
description: 'Дополнительные сведения о: IF1 и IF2'
title: IF1 и IF2
ms.date: 11/21/2019
f1_keywords:
- IF2
- IF1
helpviewer_keywords:
- IF2 directive
- IF2 directive
ms.assetid: a0f75564-b51b-4e39-ad3b-f7421e7ecad6
ms.openlocfilehash: 427edae687846f19aa281db2b625c8cdf68a1707
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97130199"
---
# <a name="if1-and-if2"></a>IF1 и IF2

Блок **IF1** вычисляется на первом этапе сборки.

Блок **If2** вычисляется на каждой сборке Pass, если **параметр: SETIF2** имеет **значение true**.

## <a name="syntax"></a>Синтаксис

> **IF1;;**

> **IF2;;**

## <a name="remarks"></a>Комментарии

Полный [Синтаксис см.](if-masm.md) в разделе.

В отличие от версии 5,1, MASM 6,1 и выше выполняет большую часть работы по его первому проходу, а затем выполнит столько последующих проходов, сколько необходимо. Напротив, компилятор MASM 5,1 всегда собирается в двух исходных проходах. В результате может потребоваться изменить или удалить некоторые зависящие от передаваемых конструкций в MASM 6,1 и более поздних версиях.

### <a name="two-pass-directives"></a>Директивы Two-Pass

Для обеспечения совместимости компиляторы MASM 6,1 и выше поддерживают директивы 5,1, которые ссылаются на два прохода. К ним относятся **. ERR1**, **. ERR2**, **IF1**, **If2**, **ELSEIF1** и **ELSEIF2**. Для конструкций второго этапа необходимо указать [параметр SETIF2](option-masm.md). Без **параметра SETIF2 параметры** **If2** и **.** Директивы ERR2 вызывают ошибку:

```output
.ERR2 not allowed : single-pass assembler
```

Компилятор MASM 6,1 и более поздних версий обработают конструкции First-Pass иначе. Он обрабатывает **. ERR1** директиву AS **. ERR**, а директива **IF1** — как **If**.

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
