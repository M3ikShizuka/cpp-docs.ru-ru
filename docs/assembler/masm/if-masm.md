---
description: 'Дополнительные сведения: Если'
title: IF (MASM)
ms.date: 12/17/2019
helpviewer_keywords:
- IF directive
ms.assetid: 82e43712-4f0c-4bf6-90ce-0663e81af707
ms.openlocfilehash: 09b4bd09155ef848ad165b4e8b0d3a093ade0008
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97130213"
---
# <a name="if"></a>IF

Предоставляет сборку *ифстатементс* , если *expression1* имеет значение true (отличное от нуля) или *елсеифстатементс* , если *expression1* имеет значение false (0), а *Expression2* имеет значение true.

## <a name="syntax"></a>Синтаксис

> **Если** *expression1*\
> *операторы If*\
> ⟦**ELSEIF** , *выражение2*\
> *ElseIf-операторы*⟧ \
> ⟦**Else**\
> *else-Операторы*⟧ \
> **ENDIF**

## <a name="remarks"></a>Комментарии

Следующие директивы могут быть заменены на [ElseIf](elseif-masm.md): **елсеифб**, **елсеифдеф**, **елсеифдиф**, **елсеифдифи**, **ELSEIF**, **елсеифидн**, **елсеифидни**, **елсеифнб** и **елсеифндеф**. При необходимости собирает *else-Операторы* , если предыдущее выражение имеет значение false. Обратите внимание, что выражения оцениваются во время сборки.

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
