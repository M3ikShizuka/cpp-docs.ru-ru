---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4206'
title: Предупреждение средств компоновщика LNK4206
ms.date: 12/05/2017
f1_keywords:
- LNK4206
helpviewer_keywords:
- LNK4206
ms.assetid: 6c108e33-00cf-4c5a-830d-d65d470930a7
ms.openlocfilehash: 40d7a8f18a835721ff747293696d0499c0a94ef3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294149"
---
# <a name="linker-tools-warning-lnk4206"></a>Предупреждение средств компоновщика LNK4206

> не найдены сведения о предкомпилированном типе; *файл "имяфайла*" не связан или перезаписан; Компоновка объекта как при отсутствии отладочной информации

Объект *filename* , скомпилированный с помощью [/Yc](../../build/reference/yc-create-precompiled-header-file.md), был либо не указан в команде LINK, либо был перезаписан.

Распространенным сценарием для этого предупреждения является ситуация, когда OBJ-объект, скомпилированный с параметром/Yc, находится в библиотеке и в котором нет ссылок на символы этого obj из кода.  В этом случае компоновщик не будет использовать (или даже просматривать) OBJ-файл.  В этом случае следует выполнить повторную компиляцию кода и использовать параметр [/Yl](../../build/reference/yl-inject-pch-reference-for-debug-library.md) для объектов, скомпилированных с помощью [/Yu](../../build/reference/yu-use-precompiled-header-file.md).
