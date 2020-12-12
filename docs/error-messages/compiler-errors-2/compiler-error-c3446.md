---
description: 'Дополнительные сведения о: Ошибка компилятора C3446'
title: Ошибка компилятора C3446
ms.date: 07/21/2017
f1_keywords:
- C3446
helpviewer_keywords:
- C3446
ms.assetid: 33064548-24e4-46f1-beb1-476e3c3b3fbf
ms.openlocfilehash: 442ac07c1684278e76f86531d1c28de6507eb999
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97113677"
---
# <a name="compiler-error-c3446"></a>Ошибка компилятора C3446

>"*класс*": инициализатор членов по умолчанию не допускается для члена класса значений

В Visual Studio 2015 и более ранних версиях компилятор допускал (но игнорировал) инициализатор членов по умолчанию для члена класса значений. Инициализатор по умолчанию для класса значений всегда инициализирует члены нулевым значением. Конструктор по умолчанию не допускается. В Visual Studio 2017 инициализаторы членов по умолчанию вызывают ошибку компилятора, как показано в следующем примере:

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3446 в Visual Studio 2017 и более поздних версий:

```cpp
// C3446.cpp
value struct V
{
       int i = 0; // error C3446: 'V::i': a default member initializer
                  // is not allowed for a member of a value class
       int j {0}; // C3446
};
```

Чтобы исправить эту ошибку, удалите инициализатор:

```cpp
// C3446b.cpp
value struct V
{
       int i;
       int j;
};
```
