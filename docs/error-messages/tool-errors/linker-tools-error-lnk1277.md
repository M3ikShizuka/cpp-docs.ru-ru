---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1277'
title: Ошибка средств компоновщика LNK1277
ms.date: 11/04/2016
f1_keywords:
- LNK1277
helpviewer_keywords:
- LNK1277
ms.assetid: afca3de0-50cc-4140-af7a-13493a170835
ms.openlocfilehash: 82a71878d30088bd018c4e54216d53228efe949d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193738"
---
# <a name="linker-tools-error-lnk1277"></a>Ошибка средств компоновщика LNK1277

запись объекта не найдена в PGD (имя файла)

При использовании [/LTCG: пгоптимзе](../../build/reference/ltcg-link-time-code-generation.md)путь к одному из файлов input. lib, DEF или obj отличается от пути, в котором они были найдены во время/LTCG: PGINSTRUMENT. Это можно объяснить путем изменения переменной среды LIB после/LTCG: PGINSTRUMENT. Полный путь к входным файлам хранится в PGD-файле.

Параметр/LTCG: PGOPTIMIZE требует, чтобы входные данные совпадали с фазой/LTCG: PGINSTRUMENT.

Чтобы устранить это предупреждение, выполните одно из следующих действий.

- Выполните команду/LTCG: PGINSTRUMENT, повторите все тестовые запуски и выполните/LTCG: PGOPTIMIZE.

- Измените переменную среды LIB, чтобы она находилась при выполнении/LTCG: PGINSTRUMENT.

Не рекомендуется обойти LNK1277 с помощью/LTCG: PGUPDATE.
