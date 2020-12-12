---
description: 'Дополнительные сведения о: Ошибка компилятора C3218'
title: Ошибка компилятора C3218
ms.date: 11/04/2016
f1_keywords:
- C3218
helpviewer_keywords:
- C3218
ms.assetid: 0eea19e0-503e-4e07-ae8b-2cb2e95922cd
ms.openlocfilehash: 9b8b3ed9fdd0fa2632435f4afd9d6ef9bb39b49b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97173705"
---
# <a name="compiler-error-c3218"></a>Ошибка компилятора C3218

"тип": тип не допускается в качестве ограничения

Чтобы тип был ограничением, он должен быть либо типом значения, либо ссылкой на управляемый класс или интерфейс.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3218.

```cpp
// C3218.cpp
// compile with: /clr /c
class A {};
ref class B {};

// Delete the following 3 lines to resolve.
generic <class T>
where T : A   // C3218
ref class C {};

// OK
generic <class T>
where  T : B
ref class D {};
```
