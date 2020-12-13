---
description: 'Дополнительные сведения: Ошибка компилятора ресурсов ресурсов RC2148'
title: Ошибка компилятора ресурсов RC2148
ms.date: 11/04/2016
f1_keywords:
- RC2148
helpviewer_keywords:
- RC2148
ms.assetid: 0290065c-35d3-4815-80c5-40bf7132ae1d
ms.openlocfilehash: 10d20fe175005794fd10a84d2817024dea7e630c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97133423"
---
# <a name="resource-compiler-error-rc2148"></a>Ошибка компилятора ресурсов RC2148

Идентификатор языка слишком велик

Значение идентификатора языка выходит за пределы допустимого диапазона.

Оператор **LANGUAGE** должен использовать следующий синтаксис:

**LANGUAGE** *ИД_основного_языка*,*ИД_дополнительного_языка*

Допустимые идентификаторы языков определяются как **SUBLANG_** константы в файле WINNT. h.
