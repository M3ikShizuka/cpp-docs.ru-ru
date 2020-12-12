---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1264'
title: Ошибка средств компоновщика LNK1264
ms.date: 11/04/2016
f1_keywords:
- LNK1264
helpviewer_keywords:
- LNK1264
ms.assetid: 23b1aad7-d382-42c1-bae8-db68575c57a8
ms.openlocfilehash: 122186482800597780405ae89e8e01c008794756
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193790"
---
# <a name="linker-tools-error-lnk1264"></a>Ошибка средств компоновщика LNK1264

Указан параметр/LTCG: PGINSTRUMENT, но создание кода не требуется; Сбой инструментирования

Указан параметр **/LTCG: PGINSTRUMENT** , но не найдены OBJ-файлы, скомпилированные с помощью [/GL](../../build/reference/gl-whole-program-optimization.md). Невозможно выполнить инструментирование, так как произошел сбой связи. В командной строке должен быть хотя бы один OBJ-файл, скомпилированный с параметром **/GL** , чтобы можно было выполнить инструментирование.

Профильная оптимизация (PGO) доступна только в 64-разрядных компиляторах.
