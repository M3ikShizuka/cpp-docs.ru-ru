---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4092'
title: Предупреждение компилятора (уровень 4) C4092
ms.date: 11/04/2016
f1_keywords:
- C4092
helpviewer_keywords:
- C4092
ms.assetid: 396ae826-a892-4327-bd66-f4762376d72b
ms.openlocfilehash: 70b2d94304863610ede64a30bcb1bb6d407f2e12
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97262016"
---
# <a name="compiler-warning-level-4-c4092"></a>Предупреждение компилятора (уровень 4) C4092

> sizeof возвращает "unsigned long"

Операнд **`sizeof`** оператора был очень большим, поэтому **`sizeof`** возвращает **`unsigned long`** . Это предупреждение появляется в разделе расширения Майкрософт ( [`/Ze`](../../build/reference/za-ze-disable-language-extensions.md) ). В режиме совместимости с ANSI ( **`/Za`** ) результат усекается.
