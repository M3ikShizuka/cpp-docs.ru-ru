---
description: 'Дополнительные сведения: Неустранимая ошибка NMAKE U1070'
title: Неустранимая ошибка NMAKE U1070
ms.date: 11/04/2016
f1_keywords:
- U1070
helpviewer_keywords:
- U1070
ms.assetid: 8639fc39-b4b1-48f5-ac91-0e9fb61680fd
ms.openlocfilehash: a3d0ee448062fec8a024501b0c08d5f0466d974b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97283528"
---
# <a name="nmake-fatal-error-u1070"></a>Неустранимая ошибка NMAKE U1070

цикл в определении макроса "имямакроса"

Заданное определение макроса содержит макрос, определение которого содержало данный макрос. Недопустимые циклические определения макросов.

## <a name="example"></a>Пример

Следующие определения макросов

```
ONE=$(TWO)
TWO=$(ONE)
```

приводит к следующей ошибке:

```
cycle in macro definition 'TWO'
```
