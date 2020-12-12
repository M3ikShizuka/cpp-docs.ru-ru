---
description: 'Дополнительные сведения: устаревшие соглашения о вызовах'
title: Устаревшие соглашения о вызовах
ms.date: 11/04/2016
f1_keywords:
- __fortran
- __pascal
- __syscall
helpviewer_keywords:
- WINAPI [C++]
- __syscall keyword [C++]
- __pascal keyword [C++]
- __fortran keyword [C++]
- calling conventions, obsolete
ms.assetid: a91fc665-034a-48ce-b6bd-d27125f308a7
ms.openlocfilehash: 0dfbb34215ba79b54d01ce12fe4d543dbe1d6859
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146046"
---
# <a name="obsolete-calling-conventions"></a>Устаревшие соглашения о вызовах

**Блок, относящийся только к системам Microsoft**

Соглашения о вызовах **__pascal**, **__fortran** и **__syscall** больше не поддерживаются. Их функциональные возможности можно эмулировать с помощью одного из поддерживаемых соглашений о вызовах и соответствующих параметров компоновщика.

\<windows.h> Теперь поддерживает макрос WINAPI, который преобразуется в соответствующее соглашение о вызовах для целевого объекта. Используйте WINAPI, где ранее использовался стиль PASCAL или **__far \_ _pascal**.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Передача аргументов и соглашения именования](../cpp/argument-passing-and-naming-conventions.md)
