---
description: 'Дополнительные сведения о: NMAKE Warning U4010'
title: Предупреждение программы NMAKE U4010
ms.date: 11/04/2016
f1_keywords:
- U4010
helpviewer_keywords:
- U4010
ms.assetid: 99d8eb9a-ae31-40d1-b8c5-8c66732127d3
ms.openlocfilehash: d0c72044576ebf3441fdec7980c933edec671097
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334791"
---
# <a name="nmake-warning-u4010"></a>Предупреждение программы NMAKE U4010

"целевой объект": сбой сборки; Указан/k, продолжение...

Команда в блоке команд для данного целевого объекта вернула ненулевой код выхода. Параметр/K сообщает NMAKE, чтобы продолжить обработку несвязанных частей сборки и выдать код выхода 1 после завершения сеанса NMAKE.

Если заданный целевой объект является, зависимым от другого целевого объекта, NMAKE выдает предупреждение [U4011](../../error-messages/tool-errors/nmake-warning-u4011.md) после этого предупреждения.
