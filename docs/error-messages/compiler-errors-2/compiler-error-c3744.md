---
description: 'Дополнительные сведения о: Ошибка компилятора C3744'
title: Ошибка компилятора C3744
ms.date: 11/04/2016
f1_keywords:
- C3744
helpviewer_keywords:
- C3744
ms.assetid: a447d050-80d1-406a-9a6e-f15c527d717c
ms.openlocfilehash: 6d8e9184db37f65fd73a85aaaa6c350303802216
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340233"
---
# <a name="compiler-error-c3744"></a>Ошибка компилятора C3744

__unhook должны иметь по крайней мере 3 аргумента для управляемых событий

[`__unhook`](../../cpp/unhook.md)Функция должна принимать три параметра при использовании в программе, компилируемой для управляемые расширения для C++.

**`__hook`** и **`__unhook`** не совместимы с **`/clr`** программированием. Вместо этого используйте операторы + = и-=.

C3744 доступен только при использовании устаревшего параметра компилятора **`/clr:oldSyntax`** .
