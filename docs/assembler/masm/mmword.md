---
description: 'Дополнительные сведения о: ММВОРД'
title: MMWORD
ms.date: 12/17/2019
f1_keywords:
- MMWORD
helpviewer_keywords:
- MMWORD directive
ms.assetid: b4c5a104-9078-4fb4-afc3-d1e63abe562a
ms.openlocfilehash: f0e888efcfea7c1ca94129ff3e4cd2f40644ae13
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97128237"
---
# <a name="mmword"></a>MMWORD

Используется для 64-разрядных операндов мультимедиа с инструкциями MMX и SSE (XMM).

## <a name="syntax"></a>Синтаксис

> **MMWORD**

## <a name="remarks"></a>Комментарии

**Ммворд** — это тип.  До **ммворд** , добавленного в MASM, эквивалентные функции могут быть достигнуты с помощью:

```asm
    mov mm0, qword ptr [ebx]
```

Хотя обе инструкции работают с 64-разрядными операндами, **QWORD** является типом для 64-разрядных целых чисел без знака, а **ммворд** — типом для значения 64-bit.

**Ммворд** предназначен для представления того же типа, что и [__m64](../../cpp/m64.md).

## <a name="example"></a>Пример

```asm
    movq     mm0, mmword ptr [ebx]
```

## <a name="see-also"></a>См. также:

[Грамматика MASM BNF](masm-bnf-grammar.md)
