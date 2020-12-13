---
description: 'Дополнительные сведения: Неустранимая ошибка NMAKE U1056'
title: Неустранимая ошибка NMAKE U1056
ms.date: 11/04/2016
f1_keywords:
- U1056
helpviewer_keywords:
- U1056
ms.assetid: da855728-b69e-413c-83ed-df912126215e
ms.openlocfilehash: beb7814d2e29665e1f92c7ef1e8dadbd66af5d63
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330375"
---
# <a name="nmake-fatal-error-u1056"></a>Неустранимая ошибка NMAKE U1056

не удается найти обработчик команд

Обработчик команд не находится в пути, указанном в переменных среды **ComSpec** или **path** .

При выполнении команд NMAKE использует COMMAND.COM или CMD.EXE в качестве обработчика команд. Он сначала ищет обработчик команд в пути, установленном в **ComSpec**. Если **ComSpec** не существует, NMAKE выполняет поиск в каталогах, указанных в параметре **path**.
