---
description: Дополнительные сведения:. ПРИВЕДЕН
title: .CODE
ms.date: 12/17/2019
f1_keywords:
- .CODE
helpviewer_keywords:
- .CODE directive
ms.assetid: 2b8c882c-c0d2-4fa3-8335-e6b12717a4f4
ms.openlocfilehash: 3f47b3bf9f345ae39f68b1b21e8f3807f554ea2d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97132280"
---
# <a name="code"></a>.CODE

(только 32-разрядный MASM.) При использовании с [. MODEL](dot-model.md)указывает начало сегмента кода.

## <a name="syntax"></a>Синтаксис

> **. КОД** ⟦*имя*⟧ \
> ⟦ *сегментитем* ⟧... \
> ⟦ *кодесегментнамеид* **заканчивается**;; ⟧\

### <a name="parameters"></a>Параметры

*безымян*\
Необязательный параметр, указывающий имя сегмента кода. Имя по умолчанию — **_TEXT** для мелких, небольших, сжатых и плоских [моделей](dot-model.md). Имя по умолчанию — *modulename* _TEXT для других моделей.

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[. DATA](dot-data.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
