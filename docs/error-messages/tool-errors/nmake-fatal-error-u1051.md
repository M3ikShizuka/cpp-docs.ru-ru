---
description: 'Дополнительные сведения: Неустранимая ошибка NMAKE U1051'
title: Неустранимая ошибка NMAKE U1051
ms.date: 11/04/2016
f1_keywords:
- U1051
helpviewer_keywords:
- U1051
ms.assetid: fede5cd5-dac3-47b7-b86d-e1acfb78699f
ms.openlocfilehash: c7d465eaf34adb69e41f523006fb0740eea722ef
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97272114"
---
# <a name="nmake-fatal-error-u1051"></a>Неустранимая ошибка NMAKE U1051

недостаточно памяти

Программе NMAKE не хватило памяти, включая виртуальную память, так как файл makefile слишком большой или сложный.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>Возможные способы устранения этой ошибки

1. Освободите место на диске.

1. Увеличьте размер файла подкачки Windows NT или файла подкачки Windows.

1. Если используется только часть файла makefile, Разделите файл makefile на отдельные файлы или используйте **.** Значение, если директивы предварительной обработки позволяют ограничить объем обработки, которую должен ОБРАБОТАТЬ NMAKE. **! Если** директивы if включают **! Если**, `!IFDEF` , **! IFNDEF**, **! ELSE IF**, **! ELSE** `IFDEF` и **! ELSE** `IFNDEF` .
