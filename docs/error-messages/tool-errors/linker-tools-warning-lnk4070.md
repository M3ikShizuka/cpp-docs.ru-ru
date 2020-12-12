---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4070'
title: Предупреждение средств компоновщика LNK4070
ms.date: 11/04/2016
f1_keywords:
- LNK4070
helpviewer_keywords:
- LNK4070
ms.assetid: f95f179a-fff9-427e-bd51-466b3934517f
ms.openlocfilehash: 188c8d88fa4fec332dad80fd5afee346f6099fca
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97210183"
---
# <a name="linker-tools-warning-lnk4070"></a>Предупреждение средств компоновщика LNK4070

/OUT: filename директива в. EXP отличается от выходного имени файла "имяфайла"; пропуск директивы

Объект, `filename` указанный в операторе [Name](../../build/reference/name-c-cpp.md) или [Library](../../build/reference/library.md) , когда файл. exp был создан, отличается от выходных данных `filename` , которые были приняты по умолчанию или указаны с помощью параметра [/out](../../build/reference/out-output-file-name.md) .

Это предупреждение появляется при изменении имени выходного файла в среде разработки и в том случае, если DEF файла проекта не был обновлен. Обновите файл. def вручную, чтобы устранить это предупреждение.

Клиентская программа, использующая полученную библиотеку DLL, может столкнуться с проблемами.
