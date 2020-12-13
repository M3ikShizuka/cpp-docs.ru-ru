---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4612'
title: Предупреждение компилятора (уровень 1) C4612
ms.date: 08/27/2018
f1_keywords:
- C4612
helpviewer_keywords:
- C4612
ms.assetid: 21ac02b2-51cd-4aff-9b70-d543511d5962
ms.openlocfilehash: 2844b54c592f5c4c4817cfec97d57c41fa2055b1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341728"
---
# <a name="compiler-warning-level-1-c4612"></a>Предупреждение компилятора (уровень 1) C4612

> ошибка в имени включаемого файла

## <a name="remarks"></a>Комментарии

Это предупреждение возникает с **#pragma include_alias** , когда имя файла указано неправильно или отсутствует.

Аргументы инструкции **#pragma include_alias** могут использовать форму кавычек ("*filename*") или форму в угловых скобках ( \<*filename*> ), но обе должны использовать одну и ту же форму.

## <a name="example"></a>Пример

```cpp
// C4612.cpp
// compile with: /W1 /LD
#pragma include_alias("StandardIO", <stdio.h>) // C4612
```
