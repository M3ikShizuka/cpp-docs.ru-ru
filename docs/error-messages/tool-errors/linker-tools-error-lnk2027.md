---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK2027'
title: Ошибка средств компоновщика LNK2027
ms.date: 11/04/2016
f1_keywords:
- LNK2027
helpviewer_keywords:
- LNK2027
ms.assetid: e2f857a8-8e8a-4697-bbff-12ccb84a35c1
ms.openlocfilehash: 006ca3b0c9d0ef85f118db9b562e8228c7cad238
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97275767"
---
# <a name="linker-tools-error-lnk2027"></a>Ошибка средств компоновщика LNK2027

неразрешенная ссылка на модуль "Module"

Файл, переданный компоновщику, зависит от модуля, который не был указан с помощью **/ASSEMBLYMODULE** , и не передается непосредственно компоновщику.

Чтобы разрешить LNK2027, выполните одно из следующих действий.

- Не передавайте компоновщику файл, имеющий зависимость модуля.

- Укажите модуль с **/ASSEMBLYMODULE**.

- Если модуль является типобезопасным. netmodule, передайте модуль непосредственно в компоновщик.

Дополнительные сведения см. в разделе [/ASSEMBLYMODULE (Добавление модуля MSIL в сборку)](../../build/reference/assemblymodule-add-a-msil-module-to-the-assembly.md) и [NETMODULE-файлы в качестве входных файлов компоновщика](../../build/reference/netmodule-files-as-linker-input.md).
