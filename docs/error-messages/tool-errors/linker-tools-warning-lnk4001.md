---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4001'
title: Предупреждение средств компоновщика LNK4001
ms.date: 11/04/2016
f1_keywords:
- LNK4001
helpviewer_keywords:
- LNK4001
ms.assetid: 0a8b1c3a-64ce-4311-b7c0-065995059246
ms.openlocfilehash: ceae4b205a7d591eff6de6c745fc379d5422a0e0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332038"
---
# <a name="linker-tools-warning-lnk4001"></a>Предупреждение средств компоновщика LNK4001

не указаны объектные файлы. используемые библиотеки

Компоновщик передал один или несколько LIB-файлов, но не имеет OBJ-файлов.

Так как компоновщик не может получить доступ к информации в LIB-файле, к которой он может получить доступ в OBJ-файле, это предупреждение означает, что вам придется явно указать другие параметры компоновщика. Например, может потребоваться указать параметры [/Machine](../../build/reference/machine-specify-target-platform.md), [/out](../../build/reference/out-output-file-name.md)или [/entry](../../build/reference/entry-entry-point-symbol.md) .
