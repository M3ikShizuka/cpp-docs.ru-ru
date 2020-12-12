---
description: Дополнительные сведения о запуске программы в предварительной обработке
title: Выполнение программ в ходе предварительной обработки
ms.date: 11/04/2016
helpviewer_keywords:
- program execution [C++]
ms.assetid: 5ecf123a-20e5-40cd-b8d8-dd5a9fdd4b24
ms.openlocfilehash: 72743fe1b75e170ce1aa7ea04dd5a0c70440de59
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192373"
---
# <a name="executing-a-program-in-preprocessing"></a>Выполнение программ в ходе предварительной обработки

Чтобы использовать код выхода команды во время предварительной обработки, укажите команду с любыми аргументами в квадратных скобках ([]). Все макросы развертываются до выполнения команды. NMAKE заменяет спецификацию команды кодом выхода команды, который можно использовать в выражении для управления предварительной обработкой.

## <a name="see-also"></a>См. также раздел

[Выражения в предварительной обработке файла makefile](expressions-in-makefile-preprocessing.md)
