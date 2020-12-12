---
description: 'Дополнительные сведения о: NMAKE Warning U4011'
title: Предупреждение программы NMAKE U4011
ms.date: 11/04/2016
f1_keywords:
- U4011
helpviewer_keywords:
- U4011
ms.assetid: e8244514-eba6-4285-8853-7baeefdcd8a4
ms.openlocfilehash: b421dff75ea0ecbdbc454053db3912e3f3e47ded
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97164241"
---
# <a name="nmake-warning-u4011"></a>Предупреждение программы NMAKE U4011

' target ': доступны не все зависимые объекты; Целевой объект не построен

Зависимая от данного целевого объекта либо не существует, либо устарела, а команда для обновления зависимого кода вернула ненулевой код выхода. Параметр/K сообщает NMAKE, чтобы продолжить обработку несвязанных частей сборки и выдать код выхода 1 после завершения сеанса NMAKE.

Этому предупреждению предшествует предупреждение [U4010](../../error-messages/tool-errors/nmake-warning-u4010.md) для каждого зависимого, которое не удалось создать или обновить.
