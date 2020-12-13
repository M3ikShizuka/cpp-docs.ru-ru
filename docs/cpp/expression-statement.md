---
description: 'Дополнительные сведения: оператор expression'
title: Оператор выражений
ms.date: 11/04/2016
helpviewer_keywords:
- statements [C++], expression
- expression statements
ms.assetid: 547d7f7a-58be-4ffc-a4b3-d64c7ae7538c
ms.openlocfilehash: a208951c536883f2f08a6e856e9da48884255b1a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97186549"
---
# <a name="expression-statement"></a>Оператор выражений

Операторы выражений обеспечивают вычисление выражений. В результате выполнения оператора выражения ни передачи управления, ни итерации не происходит.

Синтаксис оператора выражения простой:

## <a name="syntax"></a>Синтаксис

```
[expression ] ;
```

## <a name="remarks"></a>Remarks

Вычисление всех выражений в операторе выражения и учет всех побочных эффектов осуществляются до выполнения следующего оператора. Самые распространенные операторы выражений — присваивания и вызовы функций.  Поскольку выражение является необязательным, только точка с запятой считается пустым оператором выражения, называемой оператором [null](../cpp/null-statement.md) .

## <a name="see-also"></a>См. также раздел

[Общие сведения о инструкциях C++](../cpp/overview-of-cpp-statements.md)
