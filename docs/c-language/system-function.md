---
description: Подробнее о функции system
title: Функция system
ms.date: 11/04/2016
helpviewer_keywords:
- system function
ms.assetid: 0786ccdc-20cd-4d96-b3d8-3230507c3066
ms.openlocfilehash: 094fb3be58c1ff82c823ff79c4181a46b7ddf14c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97114384"
---
# <a name="system-function"></a>Функция system

**ANSI 4.10.4.5** Содержимое и режим выполнения строки функцией **system**

Функция **system** выполняет внутреннюю команду операционной системы или файл .EXE, .COM (.CMD в Windows NT) или .BAT прямо из программы на языке C, а не в режиме командной строки.

Функция system находит интерпретатор команд (обычно это CMD.EXE в Windows NT или COMMAND.COM в Windows). Затем функция system передает строку аргумента в интерпретатору команд.

Дополнительные сведения см. в описании [system, _wsystem](../c-runtime-library/reference/system-wsystem.md).

## <a name="see-also"></a>См. также

[Функции библиотеки](../c-language/library-functions.md)
