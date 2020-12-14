---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1107'
title: Ошибка средств компоновщика LNK1107
ms.date: 11/04/2016
f1_keywords:
- LNK1107
helpviewer_keywords:
- LNK1107
ms.assetid: a37a893d-5efa-4eba-8f40-6c5518b4b9d0
ms.openlocfilehash: 2a5ed9ba0bc4789a324d143b6287a08712299cdd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97281396"
---
# <a name="linker-tools-error-lnk1107"></a>Ошибка средств компоновщика LNK1107

Недопустимый или поврежденный файл: не удается прочитать в расположении

Средству не удалось прочитать файл. Повторно создайте файл.

LNK1107 также может возникнуть при попытке передать компоновщику модуль (DLL или. netmodule, созданный с [параметром/clr: Assembly](../../build/reference/clr-common-language-runtime-compilation.md) или  [/NOASSEMBLY](../../build/reference/noassembly-create-a-msil-module.md)); Вместо этого передайте OBJ-файл.

При компиляции следующего образца:

```cpp
// LNK1107.cpp
// compile with: /clr /LD
public ref class MyClass {
public:
   void Test(){}
};
```

а затем указать **link LNK1107.dll** в командной строке, вы получите LNK1107.  Чтобы устранить эту ошибку, укажите **link LNK1107. obj** .
