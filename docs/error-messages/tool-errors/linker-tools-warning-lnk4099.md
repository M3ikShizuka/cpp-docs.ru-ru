---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4099'
title: Предупреждение средств компоновщика LNK4099
ms.date: 11/04/2016
f1_keywords:
- LNK4099
helpviewer_keywords:
- LNK4099
ms.assetid: 358170a4-07cd-43fe-918f-82c32757ffc5
ms.openlocfilehash: 1e063cce9c884b8952e4bd5807b0d4a7683d4d54
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97133774"
---
# <a name="linker-tools-warning-lnk4099"></a>Предупреждение средств компоновщика LNK4099

PDB-файл "имяфайла" не найден с "объект/библиотека" или "путь"; Компоновка объекта как при отсутствии отладочной информации

Компоновщику не удалось найти PDB-файл. Скопируйте его в каталог, содержащий `object/library` .

Чтобы найти имя PDB-файла, связанного с объектом Object File, выполните следующие действия.

1. Извлеките объектный файл из библиотеки с помощью [lib](../../build/reference/lib-reference.md) **/Extract:** `objectname` **. obj** `xyz` **. lib**.

1. Проверьте путь к PDB-файлу с помощью **dumpbin/Section:. debug $ T/равдата** `objectname` **. obj**.

Можно также выполнить компиляцию с помощью [/Z7](../../build/reference/z7-zi-zi-debug-information-format.md), чтобы не нужно было использовать PDB, или удалите параметр компоновщика [/Debug](../../build/reference/debug-generate-debug-info.md) , если у вас нет PDB-файлов для связываемых объектов.
