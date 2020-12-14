---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK2023'
title: Ошибка средств компоновщика LNK2023
ms.date: 11/04/2016
f1_keywords:
- LNK2023
helpviewer_keywords:
- LNK2023
ms.assetid: c99e35a8-739a-4a20-a715-29b8c3744703
ms.openlocfilehash: fbcddcb00d77fd1b51effb27bc032019fc803d3c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97275819"
---
# <a name="linker-tools-error-lnk2023"></a>Ошибка средств компоновщика LNK2023

Неправильная библиотека DLL или точка входа \<dll or entry point>

Компоновщик загружает неправильную версию msobj90.dll. Убедитесь, что link.exe и msobj90.dll в пути имеют одинаковую версию.

Возможно, отсутствует зависимость msobj90.dll. Список зависимостей для msobj90.dll:

- Msvcr90.dll

- Kernel32.dll

Проверьте, не устарели ли на вашем компьютере копии msobj90.dll, которые могут устареть.
