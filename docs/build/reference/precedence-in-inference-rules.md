---
description: Дополнительные сведения см. в статье приоритет для правил вывода.
title: Приоритет правил вывода
ms.date: 11/04/2016
helpviewer_keywords:
- inference rules in NMAKE
- rules, inference
- precedence, inference rule
ms.assetid: 69e3dc02-0815-4c3a-b02b-1cb85fceaf24
ms.openlocfilehash: b56d01cce63aaaac92e011630e45bcf43e7fe0b3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225912"
---
# <a name="precedence-in-inference-rules"></a>Приоритет правил вывода

Если правило определения определяется умножением, NMAKE использует определение наивысшего приоритета. В следующем списке показан порядок приоритета от самого высокого до самого низкого:

1. Правило вывода, определенное в файле Makefile; более поздние определения имеют приоритет.

1. Правило вывода, определенное в Tools.ini; более поздние определения имеют приоритет.

1. Предопределенное правило вывода.

## <a name="see-also"></a>См. также раздел

[Правила вывода](inference-rules.md)
