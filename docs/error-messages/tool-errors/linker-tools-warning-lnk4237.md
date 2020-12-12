---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4237'
title: Предупреждение средств компоновщика LNK4237
ms.date: 11/04/2016
f1_keywords:
- LNK4237
helpviewer_keywords:
- LNK4237
ms.assetid: 87bfec39-5241-464f-9feb-517b49f352ea
ms.openlocfilehash: 9f8af2d6f0fa2d1153af749e327e95b863ed6914
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97259998"
---
# <a name="linker-tools-warning-lnk4237"></a>Предупреждение средств компоновщика LNK4237

Указан/SUBSYSTEM: NATIVE при импорте из "DLL"; Используйте/SUBSYSTEM: CONSOLE или/SUBSYSTEM: WINDOWS.

Параметр [/SUBSYSTEM: Native](../../build/reference/subsystem-specify-subsystem.md) был указан при создании приложения Windows (Win32), которое непосредственно использует один или несколько следующих компонентов:

- kernel32.dll

- gdi32.dll

- user32.dll

- Одна из \* библиотек DLL MSVCRT.

Устраните это предупреждение, не указывая **/SUBSYSTEM: Native**.
