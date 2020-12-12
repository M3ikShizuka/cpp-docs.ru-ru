---
description: 'Дополнительные сведения: несколько встроенных файлов'
title: Использование нескольких встроенных файлов
ms.date: 11/04/2016
helpviewer_keywords:
- inline files, multiple NMAKE
- multiple inline files
- NMAKE program, inline files
ms.assetid: 6d381dcf-0ed8-45d1-8df3-b4598d860b99
ms.openlocfilehash: d739591910007f69eca5d4834f6943ae0a0082ed
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190605"
---
# <a name="multiple-inline-files"></a>Использование нескольких встроенных файлов

Команда может создать более одного встроенного файла.

## <a name="syntax"></a>Синтаксис

```
command << <<
inlinetext
<<[KEEP | NOKEEP]
inlinetext
<<[KEEP | NOKEEP]
```

## <a name="remarks"></a>Remarks

Для каждого файла укажите одну или несколько строк встроенного текста, за которыми следует закрывающая строка, содержащая разделитель. Начните текст второго файла в строке, следующей за строкой разделителя для первого файла.

## <a name="see-also"></a>См. также раздел

[Встроенные файлы в файле Makefile](inline-files-in-a-makefile.md)
