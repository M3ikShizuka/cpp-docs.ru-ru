---
description: Дополнительные сведения о сопроцессоре с плавающей запятой и соглашениях о вызовах
title: Сопроцессор для вычислений с плавающей запятой и соглашения о вызовах
ms.date: 11/04/2016
helpviewer_keywords:
- floating-point numbers [C++]
- floating-point coprocessor
ms.assetid: 3cc6615a-b308-4cf7-9570-83e192a832b3
ms.openlocfilehash: 2f68671783b8a556e787aa6637b9b5c2e5799485
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97242552"
---
# <a name="floating-point-coprocessor-and-calling-conventions"></a>Сопроцессор для вычислений с плавающей запятой и соглашения о вызовах

При написании подпрограмм сборки для сопроцессора с плавающей запятой необходимо сохранить управляющее слово с плавающей запятой и очистить стек сопроцессоров, если не возвращать **`float`** **`double`** значение или (которое функция должна возвращать в St (0)).

## <a name="see-also"></a>См. также

[Соглашения о вызовах](../cpp/calling-conventions.md)
