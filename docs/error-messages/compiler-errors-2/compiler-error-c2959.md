---
description: 'Дополнительные сведения о: Ошибка компилятора C2959'
title: Ошибка компилятора C2959
ms.date: 11/04/2016
f1_keywords:
- C2959
helpviewer_keywords:
- C2959
ms.assetid: d66bb2a8-70c3-4209-a358-b0c47f111a50
ms.openlocfilehash: aa5da1db36ce8544e95ad509402b066e664faf18
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97210430"
---
# <a name="compiler-error-c2959"></a>Ошибка компилятора C2959

универсальный класс или функция не может быть членом шаблона

Дополнительные сведения см. в разделе [Среда выполнения Windows и управляемые шаблоны](../../extensions/windows-runtime-and-managed-templates-cpp-component-extensions.md) и [Общие классы](../../extensions/generics-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2959.

```cpp
// C2959.cpp
// compile with: /clr /c
template <class T> ref struct S {
   generic <class U> ref struct GR1;   // C2959
};
```
