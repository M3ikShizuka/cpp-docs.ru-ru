---
description: 'Дополнительные сведения о: Ошибка компилятора C2337'
title: Ошибка компилятора C2337
ms.date: 09/19/2019
f1_keywords:
- C2337
helpviewer_keywords:
- C2337
ms.assetid: eccc9178-a15e-42cd-bbd0-3cea7cf2d55b
ms.openlocfilehash: 44def6fe9c220699e3687ce9b843f977528b5e15
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97234856"
---
# <a name="compiler-error-c2337"></a>Ошибка компилятора C2337

> "*attribute-name*": атрибут не найден

В коде используется атрибут, который не поддерживается в данном контексте. Или атрибут недоступен в этой версии компилятора. Чтобы устранить эту проблему, Удалите неподдерживаемый атрибут.

Следующий пример приводит к возникновению ошибки C2337:

```cpp
// C2337.cpp
// compile with: /c
[emitidl];
[module(name="x")];
[grasshopper]   // C2337, not a supported attribute
class a{};
```
