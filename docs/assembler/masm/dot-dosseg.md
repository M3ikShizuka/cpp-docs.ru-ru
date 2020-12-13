---
description: Дополнительные сведения:. ДОССЕГ (32-разрядный компилятор MASM)
title: .DOSSEG
ms.date: 11/05/2019
f1_keywords:
- .DOSSEG
helpviewer_keywords:
- .DOSSEG directive
ms.assetid: 175ad470-0a2b-4e2b-b078-65e224fec040
ms.openlocfilehash: 636f3f811b20e7cf9955648c71025cfb1766fb47
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97132110"
---
# <a name="dosseg-32-bit-masm"></a>. ДОССЕГ (32-разрядный компилятор MASM)

Упорядочивает сегменты в соответствии с соглашением о сегментах MS-DOS: сначала код, затем сегменты не в ДГРАУП, а затем сегменты в ДГРАУП. (только 32-разрядный MASM.)

## <a name="syntax"></a>Синтаксис

> **. доссег**

## <a name="remarks"></a>Комментарии

Сегменты в ДГРАУП следуют в следующем порядке: сегменты не в BSS или стек, затем сегменты BSS и, наконец, сегменты СТЕКа. В основном используется для обеспечения поддержки Информация CodeView в изолированных программах MASM. То же, что и [доссег](dosseg.md).

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
