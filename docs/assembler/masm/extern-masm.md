---
description: 'Дополнительные сведения о: EXTERN'
title: EXTERN (MASM)
ms.date: 12/06/2019
helpviewer_keywords:
- EXTERN directive
ms.assetid: 667d703d-3aaf-4139-a586-29bc5dab1aff
ms.openlocfilehash: 354a390a16fb663dc6e907e37022a362c3ab5648
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97130355"
---
# <a name="extern"></a>EXTERN

Определяет одну или несколько внешних переменных, меток или символов *с именем, типом которых* является *Type*.

## <a name="syntax"></a>Синтаксис

> **Extern** ⟦*Language — Type*⟧ *Name* ⟦ __(__*АЛТИД*__)__ ⟧ __:__ *Type* ⟦__,__ ⟦*Language-Type*⟧ *Name* ⟦ __(__*АЛТИД*__)__ ⟧ __:__ *Type* ... ⟧

## <a name="remarks"></a>Комментарии

Аргумент *Language-Type* допустим только в 32-разрядном MASM.

*Тип* может быть [ABS](operator-abs.md), который импортирует *имя* как константу. То же, что и [екстрн](extrn.md).

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
