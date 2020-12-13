---
description: 'Дополнительные сведения: INVOKE'
title: INVOKE
ms.date: 11/05/2019
f1_keywords:
- Invoke
helpviewer_keywords:
- INVOKE directive
ms.assetid: 12d9bb40-33b9-411e-b801-45a1d675967e
ms.openlocfilehash: eb372ad3d7ccde9f217f55ed9817acfe9bd8f1cc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97129848"
---
# <a name="invoke"></a>INVOKE

(только 32-разрядный MASM.) Вызывает процедуру по адресу, заданному *выражением*, передавая аргументы в стеке или в регистрах в соответствии со стандартными соглашениями о вызовах типа языка.

## <a name="syntax"></a>Синтаксис

> **Вызвать** *выражение* ⟦__,__ *аргумент* ... ⟧

## <a name="remarks"></a>Комментарии

Каждый аргумент, передаваемый в процедуру, может быть выражением, парой регистров или выражением адреса (выражением с префиксом **addr**).

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
