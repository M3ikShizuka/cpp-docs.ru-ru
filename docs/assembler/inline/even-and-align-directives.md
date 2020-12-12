---
description: Дополнительные сведения о директивах и параметрах "выравнивание"
title: Директивы EVEN и ALIGN
ms.date: 08/30/2018
helpviewer_keywords:
- EVEN directive
- directives, MASM
- MASM (Microsoft Macro Assembler), directives
- NOP (no operation instruction)
- ALIGN directive
ms.assetid: 7357ab2d-4a5c-43ca-accb-a5f21cdfcde5
ms.openlocfilehash: adf633e99f1cb52a7849de24751d065a0344798f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97117800"
---
# <a name="even-and-align-directives"></a>Директивы EVEN и ALIGN

**Блок, относящийся только к системам Microsoft**

Хотя встроенный ассемблер не поддерживает большинство директив MASM, он поддерживает `EVEN` и **Выровнять**. Эти директивы помещают инструкции **NOP** (No Operation) в код сборки, необходимые для выровняйте меток по конкретным границам. В результате для некоторых процессоров операции поиска инструкций выполняются более эффективно.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Использование языка ассемблера в блоках __asm](../../assembler/inline/using-assembly-language-in-asm-blocks.md)<br/>
