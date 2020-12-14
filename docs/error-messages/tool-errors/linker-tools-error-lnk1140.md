---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1140'
title: Ошибка средств компоновщика LNK1140
ms.date: 11/04/2016
f1_keywords:
- LNK1140
helpviewer_keywords:
- LNK1140
ms.assetid: 468d7651-a7cd-47b9-aead-5bb2fab56121
ms.openlocfilehash: cde57e3594035aecc1cc3608d1329c5bc0752624
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97281201"
---
# <a name="linker-tools-error-lnk1140"></a>Ошибка средств компоновщика LNK1140

слишком много модулей для базы данных программы; связать с параметром/PDB: NONE

Проект содержит более 4096 модулей.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>Возможные способы устранения этой ошибки

1. Выполните повторную компоновку с помощью [/pdb: None](../../build/reference/pdb-use-program-database.md).

1. Скомпилируйте некоторые модули без отладочной информации.

1. Сократите число модулей.
