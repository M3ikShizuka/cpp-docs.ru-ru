---
description: 'Дополнительные сведения о: Ошибка компилятора C3235'
title: Ошибка компилятора C3235
ms.date: 11/04/2016
f1_keywords:
- C3235
helpviewer_keywords:
- C3235
ms.assetid: 0554d6c7-e1dc-4c99-8934-cbcf491c8203
ms.openlocfilehash: 5e478e9104599f833d3f63abb042660816425028
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97311907"
---
# <a name="compiler-error-c3235"></a>Ошибка компилятора C3235

"специализация": явная или частичная специализация универсального класса не допускается

Универсальные классы нельзя использовать для явных или частичных специализаций.

## <a name="example"></a>Пример

При компиляции следующего примера возникнет ошибка C3235.

```cpp
// C3235.cpp
// compile with: /clr
generic<class T>
public ref class C {};

generic<>
public ref class C<int> {};   // C3235 Remove this specialization to resolve this error.
```
