---
description: 'Дополнительные сведения о: check_stack pragma'
title: Прагма check_stack
ms.date: 08/29/2019
f1_keywords:
- vc-pragma.check_stack
- check_stack_CPP
helpviewer_keywords:
- check_stack pragma
- pragmas, check_stack
- pragmas, check_stack usage table
ms.assetid: f18e20cc-9abb-48b7-ad62-8d384875b996
ms.openlocfilehash: 55a639e22ded788bd731aad83eb7918e1006ae4c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97300857"
---
# <a name="check_stack-pragma"></a>Прагма check_stack

Указывает компилятору отключить зонды стека, если задано значение **Off** (или **-** ), или включить проверку стека, если задано значение **On** (или **+** ).

## <a name="syntax"></a>Синтаксис

> **check_stack #pragma (** [{ **On**  |  **Off** }] **)**\
> **#pragma check_stack** { **+**  |  **-** }

## <a name="remarks"></a>Комментарии

Эта директива #pragma начинает действовать с первой функции, определенной после вхождения данной директивы. Стековые зонды не являются частью макросов или функций, создаваемых как встроенные.

Если не предоставить аргумент для директивы pragma **check_stack** , проверка стека вернется к поведению, указанному в командной строке. Дополнительные сведения см. в разделе [Параметры компилятора](../build/reference/compiler-options.md). `#pragma check_stack`В следующей таблице приведены сведения о взаимодействии параметров и параметра [/GS](../build/reference/gs-control-stack-checking-calls.md) .

### <a name="using-the-check_stack-pragma"></a>Использование директивы #pragma check_stack

|Синтаксис|Скомпилировано с использованием<br /><br /> параметра /Gs?|Действие|
|------------|------------------------------------|------------|
|`#pragma check_stack( )` или<br /><br /> `#pragma check_stack`|Да|Отключает проверку стека для последующих функций|
|`#pragma check_stack( )` или<br /><br /> `#pragma check_stack`|Нет|Включает проверку стека для последующих функций|
|`#pragma check_stack(on)`<br /><br /> или `#pragma check_stack +`|"Да" или "Нет".|Включает проверку стека для последующих функций|
|`#pragma check_stack(off)`<br /><br /> или `#pragma check_stack -`|"Да" или "Нет".|Отключает проверку стека для последующих функций|

## <a name="see-also"></a>См. также раздел

[Директивы pragma и ключевое слово __pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)
