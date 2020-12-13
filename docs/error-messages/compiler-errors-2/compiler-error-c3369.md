---
description: 'Дополнительные сведения о: Ошибка компилятора C3369'
title: Ошибка компилятора C3369
ms.date: 11/04/2016
f1_keywords:
- C3369
helpviewer_keywords:
- C3369
ms.assetid: c6ceb9cb-3df9-4334-9a5c-d16db351d476
ms.openlocfilehash: 0391dbd7fe80daf93c8070253181c40fb805fa82
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97150804"
---
# <a name="compiler-error-c3369"></a>Ошибка компилятора C3369

"имя_модуля": idl_module уже определен

Использование [idl_module](../../windows/attributes/idl-module.md) там, где определяется библиотека DLL, допустимо только один раз в программе.

При компиляции следующего примера возникнет ошибка C3369:

```cpp
// C3369.cpp
// compile with: /c
[idl_module(name="name1", dllname="x.dll")]; // C3369
[idl_module(name="name1", dllname="x.dll")];
```
