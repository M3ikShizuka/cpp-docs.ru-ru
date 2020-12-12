---
description: Дополнительные сведения:/STACK
title: /STACK
ms.date: 11/04/2016
f1_keywords:
- /stack_editbin
helpviewer_keywords:
- -STACK editbin option
- STACK editbin option
- stack, setting size
- /STACK editbin option
ms.assetid: a39bcff0-c945-4355-80cc-8e4f24a5f142
ms.openlocfilehash: 253aec1d760a85f1ebe5dbf7596353b46744cd57
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97224456"
---
# <a name="stack"></a>/STACK

```
/STACK:reserve[,commit]
```

## <a name="remarks"></a>Комментарии

Этот параметр задает размер стека в байтах и принимает аргументы в десятичной или C-языковой нотации. Параметр/STACK применяется только к исполняемому файлу.

Аргумент *Reserve* задает общее выделение стека в виртуальной памяти. Программа EDITBIN Округляет указанное значение до ближайших 4 байт.

Необязательный `commit` аргумент подлежит интерпретации операционной системы. В Windows NT, Windows 95 и Windows 98 `commit` указывает объем физической памяти, выделяемой за раз. Выделенная виртуальная память приводит к тому, что пространство резервируется в файле подкачки. Более высокое `commit` значение экономит время, когда приложению требуется больше пространства стека, но при этом увеличиваются требования к памяти и, возможно, время запуска.

## <a name="see-also"></a>См. также раздел

[Параметры EDITBIN](editbin-options.md)
