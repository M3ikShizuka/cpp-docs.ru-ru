---
title: Первичные выражения в C
description: Объяснение первичных выражений в C
ms.date: 12/08/2020
helpviewer_keywords:
- primary expressions
ms.openlocfilehash: 41f011cc56f4c4fdf58c6a5fd2e3178267995854
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97300207"
---
# <a name="c-primary-expressions"></a>Первичные выражения в C

Основные выражения являются стандартными блоками более сложных выражений. Они могут быть представлены в виде констант, идентификаторов, [выделенного фрагмента _Generic](generic_selection.md) или выражения в круглых скобках.

## <a name="syntax"></a>Синтаксис

*`primary-expression`*:\
&nbsp;&nbsp;&nbsp;&nbsp;*`identifier`*\
&nbsp;&nbsp;&nbsp;&nbsp;*`constant`*\
&nbsp;&nbsp;&nbsp;&nbsp;*`string-literal`*\
&nbsp;&nbsp;&nbsp;&nbsp;**(** *`expression`* **)**\
&nbsp;&nbsp;&nbsp;&nbsp;*`generic-selection`*

*выражение*:\
&nbsp;&nbsp;&nbsp;&nbsp;*`assignment-expression`*\
&nbsp;&nbsp;&nbsp;&nbsp;*`expression`***,** *`assignment-expression`*

## <a name="see-also"></a>См. также раздел

[Выделенный фрагмент _Generic](generic_selection.md)
[Операнды и выражения](../c-language/operands-and-expressions.md)
