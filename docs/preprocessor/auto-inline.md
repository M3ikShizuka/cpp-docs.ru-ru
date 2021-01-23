---
description: Дополнительные сведения об pragma директиве auto_inline в Microsoft C/C++
title: auto_inline pragma
ms.date: 01/22/2021
f1_keywords:
- auto_inline_CPP
- vc-pragma.auto_inline
helpviewer_keywords:
- pragma, auto_inline
- auto_inline pragma
no-loc:
- pragma
ms.openlocfilehash: 72c6823acf260d48883142f8568483eb78155da1
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713731"
---
# <a name="auto_inline-no-locpragma"></a>`auto_inline` pragma

Исключает все функции, определенные в диапазоне, где **`off`** указывается как кандидаты для автоматического встраивания.

## <a name="syntax"></a>Синтаксис

> **`#pragma auto_inline(`** [ { **`on`** | **`off`** } ] **`)`**

## <a name="remarks"></a>Примечания

Чтобы использовать **`auto_inline`** pragma , разместите его до и сразу после, а не в определении функции. pragmaДействие вступает в силу сразу после того, как будет обнаружено первое определение функции после pragma .

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
