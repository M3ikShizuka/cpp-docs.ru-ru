---
description: 'Дополнительные сведения о: Ошибка компилятора C2524'
title: Ошибка компилятора C2524
ms.date: 11/04/2016
f1_keywords:
- C2524
helpviewer_keywords:
- C2524
ms.assetid: e71d17f5-2fc2-416b-8dbd-e9bed85eb33a
ms.openlocfilehash: 94e974674a5e244168499a50304a07264d23e618
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97151142"
---
# <a name="compiler-error-c2524"></a>Ошибка компилятора C2524

"деструктор": деструктор или метод завершения должен иметь список параметров "void"

Деструктор или метод завершения имел список параметров, который не является [void](../../cpp/void-cpp.md). Другие типы параметров не допускаются.

## <a name="examples"></a>Примеры

Следующий код воспроизводит C2524.

```cpp
// C2524.cpp
// compile with: /c
class A {
   A() {}
   ~A(int i) {}    // C2524
   // try the following line instead
   // ~A() {}
};
```

Следующий код воспроизводит C2524.

```cpp
// C2524_b.cpp
// compile with: /clr /c
ref struct I1 {
protected:
   !I1(int i);   // C2524
   // try the following line instead
   // !I1();
};
```
