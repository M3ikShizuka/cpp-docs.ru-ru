---
description: 'Дополнительные сведения о: Ошибка компилятора C2720'
title: Ошибка компилятора C2720
ms.date: 11/04/2016
f1_keywords:
- C2720
helpviewer_keywords:
- C2720
ms.assetid: 9ee3aab7-711b-4f5a-b2f1-cb62b130f1ce
ms.openlocfilehash: 187142af02289374235725340a206f35b6a42493
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97155661"
---
# <a name="compiler-error-c2720"></a>Ошибка компилятора C2720

> "*идентификатор*": спецификатор класса хранения "*спецификатор*" недопустим для членов

Класс хранения нельзя использовать для членов класса вне объявления. Чтобы устранить эту ошибку, удалите ненужный спецификатор [класса хранения](../../cpp/storage-classes-cpp.md) из определения члена за пределами объявления класса.

## <a name="example"></a>Пример

В следующем примере показано возникновение ошибки C2720 и приводятся сведения по ее устранению.

```cpp
// C2720.cpp
struct S {
   static int i;
};
static S::i;   // C2720 - remove the unneeded 'static' to fix it
```
