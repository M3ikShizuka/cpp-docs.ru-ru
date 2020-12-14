---
description: 'Дополнительные сведения о: Ошибка компилятора C3734'
title: Ошибка компилятора C3734
ms.date: 11/04/2016
f1_keywords:
- C3734
helpviewer_keywords:
- C3734
ms.assetid: 4e2afdcc-7da9-45a1-9c96-85f25e2986e8
ms.openlocfilehash: f24c81c06a0e140f7970e8a6fc96d90aae3780f8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245009"
---
# <a name="compiler-error-c3734"></a>Ошибка компилятора C3734

class: управляемый класс или класс WinRT не может быть коклассом

Атрибут [coclass](../../windows/attributes/coclass.md) не может использоваться с управляемыми или классами WinRT.

В следующем примере показано возникновение ошибки C3734 и приводятся сведения по ее устранению.

```cpp
// C3734.cpp
// compile with: /clr /c
[module(name="x")];

[coclass]
ref class CMyClass {   // C3734 remove the ref keyword to resolve
};
```
