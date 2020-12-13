---
description: 'Дополнительные сведения о: Ошибка компилятора C3347'
title: Ошибка компилятора C3347
ms.date: 11/04/2016
f1_keywords:
- C3347
helpviewer_keywords:
- C3347
ms.assetid: e939ad29-0b78-4681-9618-9bdae5675cee
ms.openlocfilehash: b7703865af7b081c362c110e07c2b1d3d8471129
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144564"
---
# <a name="compiler-error-c3347"></a>Ошибка компилятора C3347

"arg": обязательный аргумент не указан в атрибуте "idl_module"

Обязательный аргумент не передан в атрибут [idl_module](../../windows/attributes/idl-module.md) .

Следующий пример приводит к возникновению ошибки C3347:

```cpp
// C3347.cpp
// compile with: /c
[module(name="xx")];

[idl_module(dllname="x")];    // C3347
// try the following line instead
// [idl_module(name="test", dllname="x")];
```
