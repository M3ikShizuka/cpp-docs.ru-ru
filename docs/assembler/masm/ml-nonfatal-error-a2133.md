---
description: 'Дополнительные сведения: МАШИНное неустранимое сообщение об ошибке A2133'
title: Некритичная ошибка ML A2133
ms.date: 12/17/2019
ms.custom: error-reference
f1_keywords:
- A2133
helpviewer_keywords:
- A2133
ms.assetid: 5ba50911-22c8-43b7-90e2-946fc612e05f
ms.openlocfilehash: 11a2d27a00ac4e1d8b669ec7a7d4fe523476b5c4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97128470"
---
# <a name="ml-nonfatal-error-a2133"></a>Некритичная ошибка ML A2133

**значение регистра, Перезаписанное функцией INVOKE**

Регистр был передан в процедуру в качестве аргумента, но код, созданный функцией [Invoke](invoke.md) для передачи других аргументов, привел к удалению содержимого регистра.

Для преобразования данных ассемблером можно использовать регистры AX, AL, AH, EAX, DX, DL, DH и EDX.

Используйте другой регистр.

## <a name="see-also"></a>См. также раздел

[Сообщения об ошибках ML](ml-error-messages.md)
