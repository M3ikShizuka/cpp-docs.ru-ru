---
description: 'Дополнительные сведения: Неустранимая ошибка машинного обучения A1011'
title: Неустранимая ошибка ML A1011
ms.date: 12/17/2019
ms.custom: error-reference
f1_keywords:
- A1011
helpviewer_keywords:
- A1011
ms.assetid: 7fbf092d-4189-4330-a884-dfa2268fc3dd
ms.openlocfilehash: 294ca2cbf512948514317589628969a3e63e71af
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97129497"
---
# <a name="ml-fatal-error-a1011"></a>Неустранимая ошибка ML A1011

**Директива должна находиться в блоке управления**

Ассемблер обнаружил директиву высокого уровня, где она не ожидалась. Обнаружена одна из следующих директив:

- [. ELSE](dot-else.md) без [. Если](dot-if.md)

- [. ENDIF](dot-endif.md) без [. Если](dot-if.md)

- [. ЕНДВ](dot-endw.md) без [. Во время выполнения](dot-while.md)

- [. УНТИЛККСЗ](dot-untilcxz.md) без [. ПОВТОРИТЬ](dot-repeat.md)

- [. ПРОДОЛЖИТЬ](dot-continue.md) без [. WHILE](dot-while.md) или [. ПОВТОРИТЬ](dot-repeat.md)

- [. Прервать](dot-break.md) без [. WHILE](dot-while.md) или [. ПОВТОРИТЬ](dot-repeat.md)

- [. ЕЩЕ](dot-else.md) следующее `.ELSE`

## <a name="see-also"></a>См. также раздел

[Сообщения об ошибках ML](ml-error-messages.md)
