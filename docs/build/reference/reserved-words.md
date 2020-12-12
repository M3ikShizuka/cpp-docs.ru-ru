---
description: 'Дополнительные сведения: зарезервированные слова'
title: Зарезервированные слова
ms.date: 11/04/2016
f1_keywords:
- code
- CONFORMING
- DISCARDABLE
- Description
- base
- APPLOADER
- Data
- DYNAMIC
- DEV386
helpviewer_keywords:
- .def files [C++], reserved words
- def files [C++], reserved words
- linker [C++], reserved words
- reserved words [C++]
ms.assetid: 9b9f49e5-0739-45ab-a37e-81e3915ceb25
ms.openlocfilehash: 6d5c5971d8d01dffa1dcd1e7f6a5228fb239d4dc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225197"
---
# <a name="reserved-words"></a>Зарезервированные слова

Следующие слова зарезервированы компоновщиком. Эти имена могут использоваться в качестве аргументов в [операторах определения модуля](module-definition-dot-def-files.md) только в том случае, если имя заключено в двойные кавычки ("").

:::row:::
   :::column span="":::
      **`APPLOADER`**<sup>одного</sup>\
      **`BASE`**\
      **`CODE`**\
      **`CONFORMING`**\
      **`DATA`**\
      **`DESCRIPTION`**\
      **`DEV386`**\
      **`DISCARDABLE`**\
      **`DYNAMIC`**\
      **`EXECUTE-ONLY`**\
      **`EXECUTEONLY`**\
      **`EXECUTEREAD`**\
      **`EXETYPE`**\
      **`EXPORTS`**\
      **`FIXED`** <sup>1</sup>
   :::column-end:::
   :::column span="":::
      **`FUNCTIONS`** <sup>2</sup>\
      **`HEAPSIZE`**\
      **`IMPORTS`**\
      **`IMPURE`**<sup>одного</sup>\
      **`INCLUDE`** <sup>2</sup>\
      **`INITINSTANCE`** <sup>2</sup>\
      **`IOPL`**\
      **`LIBRARY`**<sup>одного</sup>\
      **`LOADONCALL`**<sup>одного</sup>\
      **`LONGNAMES`** <sup>2</sup>\
      **`MOVABLE`**<sup>одного</sup>\
      **`MOVEABLE`**<sup>одного</sup>\
      **`MULTIPLE`**\
      **`NAME`**\
      **`NEWFILES`** <sup>2</sup>
   :::column-end:::
   :::column span="":::
      **`NODATA`**<sup>одного</sup>\
      **`NOIOPL`**<sup>одного</sup>\
      **`NONAME`**\
      **`NONCONFORMING`**<sup>одного</sup>\
      **`NONDISCARDABLE`**\
      **`NONE`**\
      **`NONSHARED`**\
      **`NOTWINDOWCOMPAT`**<sup>одного</sup>\
      **`OBJECTS`**\
      **`OLD`**<sup>одного</sup>\
      **`PRELOAD`**\
      **`PRIVATE`**\
      **`PROTMODE`** <sup>2</sup>\
      **`PURE`**<sup>одного</sup>\
      **`READONLY`**
   :::column-end:::
   :::column span="":::
      **`READWRITE`**\
      **`REALMODE`**<sup>одного</sup>\
      **`RESIDENT`**\
      **`RESIDENTNAME`**<sup>одного</sup>\
      **`SECTIONS`**\
      **`SEGMENTS`**\
      **`SHARED`**\
      **`SINGLE`**\
      **`STACKSIZE`**\
      **`STUB`**\
      **`VERSION`**\
      **`WINDOWAPI`**\
      **`WINDOWCOMPAT`**\
      **`WINDOWS`**
   :::column-end:::
:::row-end:::

<sup>1</sup> компоновщик выдает предупреждение ("игнорируется") при обнаружении этого термина. Однако слово по-прежнему зарезервировано.

<sup>2</sup> компоновщик игнорирует это слово, но не выдает предупреждение.

## <a name="see-also"></a>См. также раздел

- [Справочник по компоновщику MSVC](linking.md)
- [Параметры компоновщика MSVC](linker-options.md)
