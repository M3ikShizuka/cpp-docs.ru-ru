---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4254'
title: Предупреждение средств компоновщика LNK4254
ms.date: 11/04/2016
f1_keywords:
- LNK4254
helpviewer_keywords:
- LNK4254
ms.assetid: 6f41dfb3-ca21-40d3-bac7-b637e578efa4
ms.openlocfilehash: 410a904af6af2015a817ac9e254dff7f09811b72
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97244476"
---
# <a name="linker-tools-warning-lnk4254"></a>Предупреждение средств компоновщика LNK4254

раздел "Section1" (offset) объединен в "section2" (offset) с различными атрибутами

Содержимое одного раздела было объединено в другой, но атрибуты двух разделов различаются. Программа может дать непредвиденные результаты. Например, данные, которые должны быть доступны только для чтения, теперь могут находиться в разделе, доступном для записи.

Чтобы разрешить LNK4254, измените или удалите запрос на слияние.

При нацеливании на компьютеры x86 и Windows CE (ARM, MIPS, SH4 и Thumb) с Visual C++,. Раздел CRT доступен только для чтения. Если код зависит от предыдущего поведения (. Разделы CRT доступны для чтения и записи. это может привести к непредвиденному поведению.

Дополнительные сведения см. в следующих разделах:

- [/MERGE (объединение разделов)](../../build/reference/merge-combine-sections.md)

- [comment (C/C++)](../../preprocessor/comment-c-cpp.md)

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки LNK4254.

```cpp
// LNK4254.cpp
// compile with: /W1 /link /WX
// LNK4254 expected
#pragma comment(linker, "/merge:.data=.text")
int main() {}
```
