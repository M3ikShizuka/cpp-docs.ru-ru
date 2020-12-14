---
description: 'Дополнительные сведения о: Ошибка компилятора C3755'
title: Ошибка компилятора C3755
ms.date: 11/04/2016
f1_keywords:
- C3755
helpviewer_keywords:
- C3755
ms.assetid: 9317b55e-a52e-4b87-b915-5a208d6eda38
ms.openlocfilehash: 24d6af223b6a15cbf1740bf67144250007c2091d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97253589"
---
# <a name="compiler-error-c3755"></a>Ошибка компилятора C3755

"Delegate": делегат не может быть определен

[Делегат (расширения компонентов C++)](../../extensions/delegate-cpp-component-extensions.md) можно объявить, но не определить.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C3755.

```cpp
// C3755.cpp
// compile with: /clr /c
delegate void MyDel() {};   // C3755
```

C3755 также может возникнуть при попытке создать шаблон делегата. Следующий пример приводит к возникновению ошибки C3755.

```cpp
// C3755_b.cpp
// compile with: /clr /c
ref struct R {
   template<class T>
   delegate void D(int) {}   // C3755
};
```
