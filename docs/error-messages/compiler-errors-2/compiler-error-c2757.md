---
description: 'Дополнительные сведения о: Ошибка компилятора C2757'
title: Ошибка компилятора C2757
ms.date: 11/04/2016
f1_keywords:
- C2757
helpviewer_keywords:
- C2757
ms.assetid: 421f102f-8a32-4d47-a109-811ddf2c909d
ms.openlocfilehash: e0be0f2a4c8dc5a5646400cbd0fa99e343ea82d5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336183"
---
# <a name="compiler-error-c2757"></a>Ошибка компилятора C2757

"символ": символ с таким именем уже существует, поэтому это имя нельзя использовать в качестве имени пространства имен

Символ, используемый в текущей компиляции в качестве идентификатора пространства имен, уже используется в сборке, на которую указывает ссылка.

Следующий пример приводит к возникновению ошибки C2757:

```cpp
// C2757a.cpp
// compile with: /clr /LD
public ref class Nes {};
```

Затем:

```cpp
// C2757b.cpp
// compile with: /clr /c
#using <C2757a.dll>

namespace Nes {    // C2757
// try the following line instead
// namespace Nes2 {
   public ref class X {};
}
```
