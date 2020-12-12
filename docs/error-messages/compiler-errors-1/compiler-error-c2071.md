---
description: 'Дополнительные сведения о: Ошибка компилятора C2071'
title: Ошибка компилятора C2071
ms.date: 11/04/2016
f1_keywords:
- C2071
helpviewer_keywords:
- C2071
ms.assetid: f8c09255-a5c4-47e3-8089-3d875ae43cc5
ms.openlocfilehash: ec5a08150b322ca5ce3a973a4e65d71ed410e25b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323198"
---
# <a name="compiler-error-c2071"></a>Ошибка компилятора C2071

'идентификатор' : недопустимый класс хранилища

`identifier` объявлено с недопустимым [классом хранения](../../c-language/c-storage-classes.md). Эта ошибка может возникнуть, когда для идентификатора указано несколько классов хранилища или когда определение несовместимо с объявлением класса хранилища.

Чтобы устранить эту проблему, изучите предполагаемый класс хранения идентификатора, например или, **`static`** **`extern`** и исправьте объявление в соответствии с ним.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C2071.

```cpp
// C2071.cpp
// compile with: /c
struct C {
   extern int i;   // C2071
};
struct D {
   int i;   // OK, no extern on an automatic
};
```

Следующий пример приводит к возникновению ошибки C2071.

```cpp
// C2071_b.cpp
// compile with: /c
typedef int x(int i) { return i; }   // C2071
typedef int (x)(int);   // OK, no local definition in typedef
```
