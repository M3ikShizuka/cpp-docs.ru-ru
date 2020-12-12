---
description: Дополнительные сведения:. FPO (32-разрядный MASM)
title: .FPO
ms.date: 11/05/2019
f1_keywords:
- .FPO
helpviewer_keywords:
- .FPO directive
ms.assetid: 35f4cd61-32f9-4262-b657-73f04f775d09
ms.openlocfilehash: 058189329cbe849086a3b1540ac7883ecac4d026
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97131707"
---
# <a name="fpo-32-bit-masm"></a>. FPO (32-разрядный MASM)

Объект **.** Директива FPO управляет эмиссией отладочных записей в сегмент. Debug $ F или раздел. (только 32-разрядный MASM.)

## <a name="syntax"></a>Синтаксис

> **. FPO** (*кдвлокалс*, *кдвпарамс*, *кбпролог*, *кбрегс*, *фусебп*, *кбфраме*)

### <a name="parameters"></a>Параметры

*кдвлокалс*\
Число локальных переменных — Неподписанное 32 разрядное значение.

*кдвпарамс*\
Размер параметров в DWORD, 16 разрядных значений без знака.

*кбпролог*\
Число байтов в коде пролога функции — 8 разрядное значение без знака.

*кбрегс*\
Число сохраняемых регистров.

*фусебп*\
Указывает, выделен ли регистр EBP. значение 0 или 1.

*кбфраме*\
Указывает тип кадра.  Дополнительные сведения см. в разделе [FPO_DATA](/windows/win32/api/winnt/ns-winnt-fpo_data) .

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
