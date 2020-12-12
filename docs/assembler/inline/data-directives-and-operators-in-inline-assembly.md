---
description: Дополнительные сведения см. в статье директивы и операторы данных во встроенном коде на языке ассемблера
title: Директивы и операторы данных во встроенном коде на языке ассемблера
ms.date: 08/30/2018
helpviewer_keywords:
- data directives [C++]
- __asm keyword [C++], referencing limitations
- MASM (Microsoft Macro Assembler), directives
- directives [C++], MASM
- MASM (Microsoft Macro Assembler), structures
- operators [MASM]
- inline assembly, operators
- inline assembly, data directives
- MASM (Microsoft Macro Assembler), operators
- structures [C++], MASM
ms.assetid: fb7410c7-156a-4131-bcfc-211aa70533e3
ms.openlocfilehash: a2b11aa95723245fc977f97f42b1de2f6c7306ac
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97117956"
---
# <a name="data-directives-and-operators-in-inline-assembly"></a>Директивы и операторы данных во встроенном коде на языке ассемблера

**Блок, относящийся только к системам Microsoft**

Хотя **`__asm`** блок может ссылаться на типы данных и объекты C или C++, он не может определять объекты данных с директивами и операторами MASM. В частности, нельзя использовать директивы определения **DB**, `DW` , **DD**,, `DQ` `DT` , и `DF` , или операторы `DUP` или.  Структуры и записи MASM также недоступны. Встроенный ассемблер не принимает директивы, `STRUC` `RECORD` , **ширину** или **маску**.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Использование языка ассемблера в блоках __asm](../../assembler/inline/using-assembly-language-in-asm-blocks.md)<br/>
