---
description: Дополнительные сведения о выражениях в предварительной обработке файлов Makefile
title: Выражения в предобработке файлов makefile
ms.date: 11/04/2016
helpviewer_keywords:
- preprocessing makefiles
- expressions [C++], makefile preprocessing
- makefiles, preprocessing
ms.assetid: 37f0f413-97e0-452c-a83f-3c9002c44c92
ms.openlocfilehash: 9b30900db493a2a87e0527e6f3c062185bb4ab43
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200797"
---
# <a name="expressions-in-makefile-preprocessing"></a>Выражения в предобработке файлов makefile

**! Если** или **! ELSE, если** `constantexpression` состоит из целочисленных констант (в десятичной или C-языковой нотации), строковых констант или команд. Используйте круглые скобки для группирования выражений. Выражения используют арифметические целые числа со знаком в стиле C; числа находятся в 32-разрядной форме с дополнительными значениями в диапазоне от-2147483648 до 2147483647.

Выражения могут использовать операторы, работающие с константными значениями, коды выхода из команд, строк, макросов и путей файловой системы.

## <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

[Операторы предварительной обработки файлов makefile](makefile-preprocessing-operators.md)

[Выполнение программ в ходе предварительной обработки](executing-a-program-in-preprocessing.md)

## <a name="see-also"></a>См. также раздел

[Предварительная обработка файла makefile](makefile-preprocessing.md)
