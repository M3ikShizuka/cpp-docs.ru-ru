---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4104'
title: Предупреждение средств компоновщика LNK4104
ms.date: 11/04/2016
f1_keywords:
- LNK4104
helpviewer_keywords:
- LNK4104
ms.assetid: ca6728db-d616-419a-a570-65e8445c6079
ms.openlocfilehash: ab48885a4a8d2806154d3a8911bdc65453359e2c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294435"
---
# <a name="linker-tools-warning-lnk4104"></a>Предупреждение средств компоновщика LNK4104

Экспорт символа "символ" должен быть частным

`symbol`Может принимать одно из следующих действий:

- `DllCanUnloadNow`

- `DllGetClassObject`

- `DllGetClassFactoryFromClassString`

- `DllGetDocumentation`

- `DllInitialize`

- `DllInstall`

- `DllRegisterServer`

- `DllRegisterServerEx`

- `DllRegisterServerExW`

- `DllUnload`

- `DllUnregisterServer`

- `RasCustomDeleteEntryNotify`

- `RasCustomDial`

- `RasCustomDialDlg`

- `RasCustomEntryDlg`

Это предупреждение выдается при построении библиотеки импорта для библиотеки DLL и экспорта одной из указанных выше функций без указания ее в качестве ЗАКРЫТой в файле определения модуля. Как правило, эти функции экспортируются для использования только OLE. Помещение их в библиотеку импорта может привести к необычному поведению, когда программа, связанная с библиотекой, неправильно выполняет вызовы. Дополнительные сведения о ключевом слове PRIVATE см. в разделе [EXPORTS](../../build/reference/exports.md).
