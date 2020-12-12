---
description: Дополнительные сведения:. сетфраме
title: .SETFRAME
ms.date: 12/17/2019
f1_keywords:
- .SETFRAME
helpviewer_keywords:
- .SETFRAME directive
ms.assetid: eaa9b5ed-4daa-4f1e-bdb6-100758007ab3
ms.openlocfilehash: b3554da14344293f00c499bc3084e6ddfd93c2ce
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97131083"
---
# <a name="setframe"></a>.SETFRAME

Заполняет поле регистра кадра и смещение в данных очистки, используя указанный регистр (*reg*) и смещение (*смещение*). Смещение должно быть кратным 16 и меньше или равно 240. Эта директива также создает `UWOP_SET_FPREG` запись кода очистки для указанного регистра, используя текущее смещение пролога.

## <a name="syntax"></a>Синтаксис

> **. СЕТФРАМЕ** *reg*, *смещение*

## <a name="remarks"></a>Комментарии

**. СЕТФРАМЕ** позволяет ml64.exe пользователям указать, каким образом должна очищаться функция Frame, и допускается только в прологе, который выходит из объявления кадра [процесса](proc.md) в [.](dot-endprolog.md) Директива ендпролог. Эти директивы не создают код. они создают только `.xdata` и `.pdata` . **. СЕТФРАМЕ** должен предшествовать инструкциям, которые фактически реализуют действия, которые должны быть развернуты. Рекомендуется заключить в оболочку как директивы очистки, так и код, предназначенный для очистки макроса, чтобы обеспечить соблюдение соглашения.

Дополнительные сведения см. в статье [MASM для x64 (ml64.exe)](masm-for-x64-ml64-exe.md).

## <a name="sample"></a>Образец

### <a name="description"></a>Описание

В следующем примере показано использование указателя фрейма:

### <a name="code"></a>Код

```asm
; ml64 frmex2.asm /link /entry:frmex2 /SUBSYSTEM:CONSOLE
_text SEGMENT
frmex2 PROC FRAME
   push rbp
.pushreg rbp
   sub rsp, 010h
.allocstack 010h
   mov rbp, rsp
.setframe rbp, 0
.endprolog
   ; modify the stack pointer outside of the prologue (similar to alloca)
   sub rsp, 060h

   ; we can unwind from the following AV because of the frame pointer
   mov rax, 0
   mov rax, [rax] ; AV!

   add rsp, 060h
   add rsp, 010h
   pop rbp
   ret
frmex2 ENDP
_text ENDS
END
```

## <a name="see-also"></a>См. также

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
