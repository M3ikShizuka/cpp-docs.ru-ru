---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4253'
title: Предупреждение средств компоновщика LNK4253
ms.date: 11/04/2016
f1_keywords:
- LNK4253
helpviewer_keywords:
- LNK4253
ms.assetid: ec7433a9-aa9c-495a-a9f2-075e7bc3e7bc
ms.openlocfilehash: 764d7698da8d724842b8387c9c4356bfce951079
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97244490"
---
# <a name="linker-tools-warning-lnk4253"></a>Предупреждение средств компоновщика LNK4253

раздел "Section1" не объединен в "section2"; уже объединено с "section3"

Компоновщик обнаружил несколько конфликтующих запросов слияния. Компоновщик будет игнорировать один из запросов.

Обнаружен параметр или директива **/Merge** , и `from` раздел уже был объединен в другой раздел из-за предыдущего параметра **/Merge** или директивы (или из-за неявного слияния компоновщика).

Чтобы разрешить LNK4253, удалите один из запросов слияния.

При нацеливании на компьютеры x86 и Windows CE (ARM, MIPS, SH4 и Thumb) с Visual C++,. Теперь раздел CRT доступен только для чтения. Если код зависит от предыдущего поведения (. Разделы CRT доступны для чтения и записи. это может привести к непредвиденному поведению.

Дополнительные сведения см. в следующих разделах:

- [/MERGE (объединение разделов)](../../build/reference/merge-combine-sections.md)

- [comment (C/C++)](../../preprocessor/comment-c-cpp.md)

## <a name="example"></a>Пример

В следующем примере компоновщику дается инструкция на слияние `.rdata` раздела дважды, но в разные разделы. Следующий пример приводит к возникновению ошибки LNK4253.

```cpp
// LNK4253.cpp
// compile with: /W1 /link /merge:.rdata=text2
// LNK4253 expected
#pragma comment(linker, "/merge:.rdata=.text")
int main() {}
```
