---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1158'
title: Ошибка средств компоновщика LNK1158
ms.date: 11/04/2016
f1_keywords:
- LNK1158
helpviewer_keywords:
- LNK1158
ms.assetid: 45febf16-d9e1-42db-af91-532e2717fd6a
ms.openlocfilehash: ea5c362de51cbf1f884f38fa4311eef557565573
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97343968"
---
# <a name="linker-tools-error-lnk1158"></a>Ошибка средств компоновщика LNK1158

не удается запустить "имяфайла"

Указанный исполняемый файл, вызываемый [Link](../../build/reference/linking.md) , не находится в каталоге, содержащем Link, или в каталоге, указанном в переменной среды PATH.

Например, эта ошибка возникает при попытке использовать параметр PGOPTIMIZE в параметре компоновщика [/LTCG](../../build/reference/ltcg-link-time-code-generation.md) на компьютере с 32-разрядной операционной системой.
