---
description: Дополнительные сведения:. аллокстакк
title: .ALLOCSTACK
ms.date: 12/17/2019
f1_keywords:
- .ALLOCSTACK
helpviewer_keywords:
- .ALLOCSTACK directive
ms.assetid: 9801594b-7ac2-4df2-a49d-07d9dd9af99e
ms.openlocfilehash: 6075b0900df104ae5faeaaff1dc0de2d3727b437
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97132370"
---
# <a name="allocstack"></a>.ALLOCSTACK

Создает **UWOP_ALLOC_SMALL** или **UWOP_ALLOC_LARGE** с указанным размером для текущего смещения в прологе.

## <a name="syntax"></a>Синтаксис

> **.** *Размер* аллокстакк

## <a name="remarks"></a>Комментарии

MASM выберет наиболее эффективную кодировку для заданного размера.

**. АЛЛОКСТАКК** позволяет ml64.exe пользователям указать, как функция Frame очищается, и допустима только в прологе, который расширяется из объявления кадра [процесса](proc.md) в [.](dot-endprolog.md) Директива ендпролог. Эти директивы не создают код. они создают только `.xdata` и `.pdata` . **. АЛЛОКСТАКК** должен предшествовать инструкциям, которые фактически реализуют действия, которые должны быть развернуты. Рекомендуется заключить в оболочку как директивы очистки, так и код, предназначенный для очистки макроса, чтобы обеспечить соблюдение соглашения.

Операнд *size* должен быть кратен 8.

Дополнительные сведения см. в статье [MASM для x64 (ml64.exe)](masm-for-x64-ml64-exe.md).

## <a name="sample"></a>Образец

В следующем примере показано, как задать обработчик очистки и исключения.

```asm
; ml64 ex3.asm /link /entry:Example1  /SUBSYSTEM:Console
text SEGMENT
PUBLIC Example3
PUBLIC Example3_UW
Example3_UW PROC NEAR
   ; exception/unwind handler body

   ret 0

Example3_UW ENDP

Example3 PROC FRAME : Example3_UW

   sub rsp, 16
.allocstack 16

.endprolog

   ; function body
    add rsp, 16
   ret 0

Example3 ENDP
text ENDS
END
```

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
