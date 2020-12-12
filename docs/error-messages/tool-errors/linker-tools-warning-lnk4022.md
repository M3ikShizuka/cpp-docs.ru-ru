---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4022'
title: Предупреждение средств компоновщика LNK4022
ms.date: 11/04/2016
f1_keywords:
- LNK4022
helpviewer_keywords:
- LNK4022
ms.assetid: 890f487e-db98-45dd-a226-c7ccead82b1e
ms.openlocfilehash: f0f968bf8e562d87e2227fb67f7a37b450c813b1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331945"
---
# <a name="linker-tools-warning-lnk4022"></a>Предупреждение средств компоновщика LNK4022

не удается найти уникальное соответствие для символа "Symbol"

LINK или LIB обнаружил несколько соответствий для заданного недекорированного символа, и ему не удалось разрешить неоднозначность. Выходной файл (exe, DLL, exp или LIB) не создается. За этим предупреждением следует одно предупреждение [LNK4002](../../error-messages/tool-errors/linker-tools-warning-lnk4002.md) для каждого повторяющегося символа, а затем — Неустранимая ошибка [LNK1152](../../error-messages/tool-errors/linker-tools-error-lnk1152.md).

Чтобы предотвратить это предупреждение, укажите символ в декорированной форме. Запустите [dumpbin](../../build/reference/dumpbin-options.md) для объекта, чтобы увидеть декорированные имена.
