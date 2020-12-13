---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1200'
title: Ошибка средств компоновщика LNK1200
ms.date: 11/04/2016
f1_keywords:
- LNK1200
helpviewer_keywords:
- LNK1200
ms.assetid: 55771145-915e-4006-ac6c-ac702041eb2f
ms.openlocfilehash: b8c380b16cef47a4b340e4a48853d58d1ab203e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341650"
---
# <a name="linker-tools-error-lnk1200"></a>Ошибка средств компоновщика LNK1200

Ошибка при чтении базы данных программы "имяфайла"

Не удалось прочитать базу данных программы (PDB).

Эта ошибка может быть вызвана повреждением файла.

Если `filename` является PDB для объектного файла, перескомпилируйте объектный файл с помощью [/Zi](../../build/reference/z7-zi-zi-debug-information-format.md).

Если `filename` является PDB для основного выходного файла и эта ошибка произошла во время добавочной компоновки, удалите PDB-файл и повторно свяжите компоновку.
