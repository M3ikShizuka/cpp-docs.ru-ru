---
description: 'Дополнительные сведения о: auto_inline pragma'
title: Прагма auto_inline
ms.date: 08/29/2019
f1_keywords:
- auto_inline_CPP
- vc-pragma.auto_inline
helpviewer_keywords:
- pragmas, auto_inline
- auto_inline pragma
ms.assetid: f7624cd1-be76-429a-881c-65c9040acf43
ms.openlocfilehash: f629bbe5dc47ba15bba5b2b55541509f421fcd8c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97301052"
---
# <a name="auto_inline-pragma"></a>Прагма auto_inline

Исключает все функции, определенные в диапазоне, где значение **Off** определяется как кандидаты для автоматического встраивания.

## <a name="syntax"></a>Синтаксис

> **auto_inline #pragma (** [{ **On**  |  **Off** }] **)**

## <a name="remarks"></a>Комментарии

Чтобы использовать директиву pragma **auto_inline** , поместите ее до и сразу после, а не внутри, определение функции. Директива pragma вступает в силу сразу после того, как будет отображено первое определение функции после директивы pragma.

## <a name="see-also"></a>См. также раздел

[Директивы pragma и ключевое слово __pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)
