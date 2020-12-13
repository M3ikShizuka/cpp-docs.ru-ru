---
description: 'Дополнительные сведения: GOTO'
title: GOTO (MASM)
ms.date: 12/16/2019
helpviewer_keywords:
- GOTO directive
ms.assetid: 6a5f73e7-6784-4eae-ac52-4fc77a7f369f
ms.openlocfilehash: ab373d77cbfb660d4cc256e39de38b7f066eac27
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97130264"
---
# <a name="goto"></a>GOTO

Передает сборку в строку, помеченную **:**_макролабел_.

## <a name="syntax"></a>Синтаксис

> **Goto** *макролабел*

## <a name="remarks"></a>Комментарии

**Оператор goto** разрешен только внутри [макросов](macro.md), [для](for-masm.md), [Форк](forc.md), [Repeat](repeat.md)и [while](while-masm.md) . Целевой объект *макролабел* должен быть единственной директивой в строке и должен предшествовать начальному двоеточию.

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
