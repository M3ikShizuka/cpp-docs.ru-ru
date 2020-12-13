---
description: 'Дополнительные сведения: макрос'
title: MACRO
ms.date: 12/16/2019
f1_keywords:
- MACRO
helpviewer_keywords:
- MACRO directive
ms.assetid: 89434f7c-bc2c-4e91-8940-fe2db8785233
ms.openlocfilehash: 5410357e76d28cddd54f3c90a34d3e85b8629143
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97129744"
---
# <a name="macro"></a>MACRO

Помечает блок макроса *именем name* и устанавливает заполнители *параметров* для аргументов, передаваемых при вызове макроса.

## <a name="syntax"></a>Синтаксис

> *имя***макроса** ⟦*параметр* ⟦**: req** | : =*аргументы по умолчанию*  |   **: VARARG**⟧... ⟧\  
> *инструкции*\
⟦**Goto** :*макролабелид*⟧ \
> ⟦**Екситм**⟧ \
> **Ендм** ⟦*значение*⟧

## <a name="remarks"></a>Комментарии

Функция-макрос возвращает *значение* в вызывающую инструкцию.

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[GOTO (MASM)](goto-masm.md)\
[ендм](endm.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
