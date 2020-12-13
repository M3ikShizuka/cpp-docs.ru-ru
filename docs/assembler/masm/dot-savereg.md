---
description: Дополнительные сведения:. саверег
title: .SAVEREG
ms.date: 12/16/2019
f1_keywords:
- .SAVEREG
helpviewer_keywords:
- .SAVEREG directive
ms.assetid: 1dbc2ef6-a197-40e7-9e55-fddcae8cef29
ms.openlocfilehash: 8b946c9b25c3f4dc6a4696b418e85487e20014eb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97131187"
---
# <a name="savereg"></a>.SAVEREG

Создает `UWOP_SAVE_NONVOL` `UWOP_SAVE_NONVOL_FAR` запись или код очистки для указанного регистра (*reg*) и смещения (*смещения*) с использованием текущего смещения пролога. MASM выберет наиболее эффективную кодировку.

## <a name="syntax"></a>Синтаксис

> **. Саверег** *reg*__,__ *смещение*

## <a name="remarks"></a>Комментарии

**. САВЕРЕГ** позволяет ml64.exe пользователям указать, как функция Frame очищается, и допустима только в прологе, который расширяется из объявления кадра [процесса](proc.md) в [.](dot-endprolog.md) Директива ендпролог. Эти директивы не создают код. они создают только `.xdata` и `.pdata` . **. САВЕРЕГ** должен предшествовать инструкциям, которые фактически реализуют действия, которые должны быть развернуты. Рекомендуется заключить в оболочку как директивы очистки, так и код, предназначенный для очистки макроса, чтобы обеспечить соблюдение соглашения.

Дополнительные сведения см. в статье [MASM для x64 (ml64.exe)](masm-for-x64-ml64-exe.md).

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
