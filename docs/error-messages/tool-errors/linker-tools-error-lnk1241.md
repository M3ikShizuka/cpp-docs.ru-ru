---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1241'
title: Ошибка средств компоновщика LNK1241
ms.date: 11/04/2016
f1_keywords:
- LNK1241
helpviewer_keywords:
- LNK1241
ms.assetid: 7b8b52eb-0231-4521-b52a-2bce8d3e8956
ms.openlocfilehash: abc72b70af9ab694744a91a8789207055bd1a5bb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193933"
---
# <a name="linker-tools-error-lnk1241"></a>Ошибка средств компоновщика LNK1241

файл ресурсов "файл ресурсов" уже указан

Эта ошибка возникает при запуске **CVTRES** вручную из командной строки и при передаче результирующего OBJ-файла компоновщику в дополнение к другим RES-файлам.

Чтобы указать несколько RES-файлов, передайте их в компоновщик как RES-файлы, а не в OBJ-файлы, созданные с помощью **CVTRES**.
