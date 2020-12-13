---
description: 'Дополнительные сведения о: Ошибка компилятора C2383'
title: Ошибка компилятора C2383
ms.date: 11/04/2016
f1_keywords:
- C2383
helpviewer_keywords:
- C2383
ms.assetid: 6696221d-879c-477a-a0f3-a6edc15fd3d7
ms.openlocfilehash: 862346d7f2bfe92a5d2182a7fe53f260b357ad0b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185938"
---
# <a name="compiler-error-c2383"></a>Ошибка компилятора C2383

"*символ*": аргументы по умолчанию не разрешены для этого символа

Компилятор C++ не разрешает использовать аргументы по умолчанию для указателей на функции.

Этот код был принят компилятором Microsoft C++ в версиях, предшествующих Visual Studio 2005, но теперь выдает ошибку. Для кода, который работает во всех версиях Visual C++, не присваивайте аргументу указателя на функцию значение по умолчанию.

## <a name="example"></a>Пример

В следующем примере создается C2383 и демонстрируется возможное решение:

```cpp
// C2383.cpp
// compile with: /c
void (*pf)(int = 0);   // C2383
void (*pf)(int);   // OK
```
