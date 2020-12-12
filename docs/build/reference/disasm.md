---
description: Дополнительные сведения о:/DISASM
title: /DISASM
ms.date: 01/17/2018
f1_keywords:
- /disasm
helpviewer_keywords:
- -DISASM dumpbin option
- DISASM dumpbin option
- /DISASM dumpbin option
ms.openlocfilehash: 764754e017958a57afd53236b7fc1ffb6217d850
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192906"
---
# <a name="disasm"></a>/DISASM

Распечатайте Дизассемблированный код разделов кода в выходных данных DUMPBIN.

## <a name="syntax"></a>Синтаксис

> **/DISASM**{**:** байтов в байтах \[  | ]}

### <a name="arguments"></a>Аргументы

**БАЙТ**<br/>
Включает байты инструкций вместе с интерпретируемыми кодом операций и аргументами в выходных данных дизассемблированного кода. Это параметр по умолчанию.

**Число байтов**<br/>
Не включает байты инструкций в выходных данных дизассемблированного кода.

## <a name="remarks"></a>Комментарии

Параметр **/DISASM** отображает Дизассемблированный код разделов кода в файле. Он использует отладочные символы, если они есть в файле.

**/DISASM** следует использовать только в собственных, не управляемых изображениях. Эквивалентным средством для управляемого кода является [Ildasm](/dotnet/framework/tools/ildasm-exe-il-disassembler).

Для использования в файлах, создаваемых параметром компилятора [/GL (оптимизация всей программы)](gl-whole-program-optimization.md) [, доступен только параметр DUMPBIN.](headers.md)

## <a name="see-also"></a>См. также раздел

[Параметры DUMPBIN](dumpbin-options.md)
