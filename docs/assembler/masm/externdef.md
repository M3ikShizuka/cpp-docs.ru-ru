---
description: 'Дополнительные сведения о: ЕКСТЕРНДЕФ'
title: EXTERNDEF
ms.date: 12/06/2019
f1_keywords:
- EXTERNDEF
helpviewer_keywords:
- EXTERNDEF directive
ms.assetid: 95a10de6-c345-4428-a2f2-90f7d411dc86
ms.openlocfilehash: b0ffc2154996fc7cea9f0b61917cadf7b776972f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97130329"
---
# <a name="externdef"></a>EXTERNDEF

Определяет одну или несколько внешних переменных, меток или символов *с именем, типом которых* является *Type*.

## <a name="syntax"></a>Синтаксис

> **Екстерндеф** ⟦*Language — введите* *имя ⟧*__:__*Type* ⟦__,__ ⟦*Language-Type*⟧ *Name*__:__*Type* ... ⟧

## <a name="remarks"></a>Комментарии

Аргумент *Language-Type* допустим только в 32-разрядном MASM.

Если *имя* определено в модуле, оно считается [открытым](public-masm.md). Если в модуле есть ссылка на *имя* , он рассматривается как [внешний](extern-masm.md). Если ссылка на *имя* не указана, она игнорируется. *Тип* может быть [ABS](operator-abs.md), который импортирует *имя* как константу. Обычно используется в включаемых файлах.

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
