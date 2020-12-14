---
description: 'Дополнительные сведения о: Ошибка компилятора C2946'
title: Ошибка компилятора C2946
ms.date: 11/04/2016
f1_keywords:
- C2946
helpviewer_keywords:
- C2946
ms.assetid: c86dfbfc-7702-4f09-8a53-d205710e99c2
ms.openlocfilehash: 7a74b17c10acd55a254c0d7fba5c8269689e3094
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97249507"
---
# <a name="compiler-error-c2946"></a>Ошибка компилятора C2946

явное создание экземпляра; "класс" не является специализацией класса-шаблона

Нельзя явно создать экземпляр класса без шаблона.

## <a name="example"></a>Пример

При компиляции следующего примера возникнет ошибка C2946.

```cpp
// C2946.cpp
class C {};
template C;  // C2946
int main() {}
```
