---
description: 'Подробнее о следующем: Постфиксные операторы увеличения и уменьшения в C'
title: Постфиксные операторы увеличения и уменьшения в C
ms.date: 11/04/2016
helpviewer_keywords:
- increment operators, syntax
- scalar operators
- types [C], scalar
ms.assetid: 56ba218d-65f9-405f-8684-caccc0ca33aa
ms.openlocfilehash: e5e230f1e1e51a1f48b29436705f4f645be9ed44
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97300220"
---
# <a name="c-postfix-increment-and-decrement-operators"></a>Постфиксные операторы увеличения и уменьшения в C

Операнды операторов постфиксных инкремента и декремента являются скалярными типами, представляющими собой изменяемые L-значения.

## <a name="syntax"></a>Синтаксис

*postfix-expression*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*postfix-expression*  **++**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*postfix-expression*  **--**

Результатом операции постфиксного инкремента или декремента является значение операнда. После получения результата значение операнда инкрементируется (или декрементируется). В следующем примере кода демонстрируется оператор постфиксного инкремента.

```
if( var++ > 0 )
    *p++ = *q++;
```

В этом примере переменная `var` сравнивается с нулем и затем инкрементируется. Если значение `var` до инкрементирования было положительным, выполняется следующий оператор. Сначала значение объекта, на который указывает `q`, присваивается объекту, на который указывает `p`. Затем `q` и `p` инкрементируются.

## <a name="see-also"></a>См. также

[Постфиксные операторы увеличения и уменьшения: ++ и --](../cpp/postfix-increment-and-decrement-operators-increment-and-decrement.md)
