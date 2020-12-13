---
description: 'Дополнительные сведения о: Command-Line Warning D9027'
title: Предупреждение командной строки D9027
ms.date: 11/04/2016
f1_keywords:
- D9027
helpviewer_keywords:
- D9027
ms.assetid: 2a29edc5-5649-48f2-9058-2057c747284c
ms.openlocfilehash: 8c17750f3310072f8f69c77587a1c17fc9377e79
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97136114"
---
# <a name="command-line-warning-d9027"></a>Предупреждение командной строки D9027

исходный файл " \<filename> " проигнорирован

CL.exe проигнорировал входной исходный файл.

Это предупреждение может быть вызвано пробелом между параметром/FO и выходным именем в командной строке с параметром/c. Пример:

```
cl /c /Fo output.obj input.c
```

Поскольку имеется пробел между/FO и `output.obj` , CL.exe принимает в `output.obj` качестве имени входного файла. Чтобы устранить эту проблему, удалите пробел:

```
cl /c /Fooutput.obj input.c
```
