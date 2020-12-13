---
description: 'Дополнительные сведения: Неустранимая ошибка NMAKE U1099'
title: Неустранимая ошибка NMAKE U1099
ms.date: 11/04/2016
f1_keywords:
- U1099
helpviewer_keywords:
- U1099
ms.assetid: 6688a805-43e6-4247-a2d0-14be082f0b13
ms.openlocfilehash: 8044010cf967e4fe27b2235968022023d66ae1c3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97345320"
---
# <a name="nmake-fatal-error-u1099"></a>Неустранимая ошибка NMAKE U1099

переполнение стека

Обрабатываемый файл makefile слишком сложен для текущего выделения стека в NMAKE. NMAKE имеет выделение 0x3000 (12K).

Чтобы увеличить выделение стека NMAKE, запустите служебную программу [EDITBIN/Stack](../../build/reference/stack.md) с большим параметром стека:

**EDITBIN/STACK: Reserve NMAKE.EXE**

где *Reserve* — это число, большее, чем текущее выделение стека в NMAKE.
