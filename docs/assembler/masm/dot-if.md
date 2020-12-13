---
description: Дополнительные сведения:. Если (32-разрядный MASM)
title: .IF
ms.date: 11/05/2019
f1_keywords:
- .IF
helpviewer_keywords:
- .IF directive
ms.assetid: dccc7615-8fc7-4829-9f39-0ee405f6c1e3
ms.openlocfilehash: e6ce9695f90a90665aee1cdaf15167963360fe04
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97131681"
---
# <a name="if-32-bit-masm"></a>. Если (32-разрядный MASM)

Создает код, который проверяет *condition1* (например, AX > 7) и выполняет *инструкции* , если это условие истинно. (только 32-разрядный MASM.)

## <a name="syntax"></a>Синтаксис

> **. Если** *condition1*\
> *инструкции*\
> ⟦**. ELSEIF** *condition2*\
> *инструкции*⟧ \
> ⟦**. ELSE**\
> *инструкции*⟧ \
> **. ENDIF**

## <a name="remarks"></a>Комментарии

Если [. В ПРОТИВном](dot-else.md) случае его операторы выполняются, если исходное условие было ложным. Обратите внимание, что условия оцениваются во время выполнения.

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
