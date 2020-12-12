---
description: 'Дополнительные сведения о: директивы макроопределения MASM во встроенном коде на языке ассемблера'
title: Директивы макросов MASM во встроенном коде на языке ассемблера
ms.date: 08/30/2018
helpviewer_keywords:
- directives, macros
- inline assembly, macro directives
- macros, directives
- MASM (Microsoft Macro Assembler), inline assembly macro directives
ms.assetid: 83643a09-1699-40a8-8ef2-13502bc4ac2c
ms.openlocfilehash: 131066ad117e0f314ba0900e8ecd19eb4843c25b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97117566"
---
# <a name="masm-macro-directives-in-inline-assembly"></a>Директивы макросов MASM во встроенном коде на языке ассемблера

**Блок, относящийся только к системам Microsoft**

Встроенный ассемблер не является ассемблером макроса. Нельзя использовать директивы макроопределения MASM (**макрос**, `REPT` , **IRC**, `IRP` и `ENDM` ) или операторы макросов ( **<>** , **!**, **&** , `%` и `.TYPE` ). **`__asm`** Однако блок может использовать директивы препроцессора C. Дополнительные сведения см. [в разделе Использование C или C++ в блоках __asm](../../assembler/inline/using-c-or-cpp-in-asm-blocks.md) .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Использование языка ассемблера в блоках __asm](../../assembler/inline/using-assembly-language-in-asm-blocks.md)<br/>
