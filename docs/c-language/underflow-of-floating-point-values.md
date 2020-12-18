---
description: 'Подробнее о следующем: Потеря точности значений с плавающей запятой'
title: Потеря точности значений с плавающей запятой
ms.date: 11/04/2016
ms.assetid: 78af8016-643c-47db-b4f1-7f06cb4b243e
ms.openlocfilehash: 3d8ddd665aa33e1c47f9f187f759058501bc5484
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321301"
---
# <a name="underflow-of-floating-point-values"></a>Потеря точности значений с плавающей запятой

**ANSI 4.5.1** Задают ли математические функции значение макроса `ERANGE` для целочисленного выражения `errno` при ошибках потери значимости

При потере точности числа с плавающей запятой выражение `errno` не получает значения `ERANGE`. Если значение стремится к нулю и, наконец, теряет значимость, значение устанавливается равным 0.

## <a name="see-also"></a>См. также

[Функции библиотеки](../c-language/library-functions.md)
