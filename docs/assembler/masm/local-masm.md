---
description: 'Дополнительные сведения: LOCAL'
title: LOCAL (MASM)
ms.date: 12/16/2019
f1_keywords:
- Local
helpviewer_keywords:
- LOCAL directive
ms.assetid: 76147e2d-23ca-4f1e-8817-81428becd113
ms.openlocfilehash: 27296f69b62de0dcd314b2575f045e06576bbf64
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97129757"
---
# <a name="local"></a>LOCAL

В первой директиве в макросе **Local** определяет метки, уникальные для каждого экземпляра макроса.

## <a name="syntax"></a>Синтаксис

> **Локальный** *LocalId* ⟦, *LocalId* ... ⟧
>
> **Локальный** *лабелид* ⟦ __\[__ *Count*__]__ ⟧ ⟦__:__*куалифиедтипе*⟧ ⟦__,__ *лабелид* ⟦ __\[__ *Count*__]__ ⟧ ⟦*куалифиедтипе*⟧... ⟧

## <a name="remarks"></a>Комментарии

Во второй директиве в определении процедуры (**proc**) **Local** создает переменные на основе стека, которые существуют в течение данной процедуры. *Лабелид* может быть простой переменной или массивом, содержащим элементы *Count* , где *Count* является константным выражением.

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
