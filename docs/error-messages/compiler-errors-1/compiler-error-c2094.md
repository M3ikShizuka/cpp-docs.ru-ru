---
description: 'Дополнительные сведения о: Ошибка компилятора C2094'
title: Ошибка компилятора C2094
ms.date: 11/04/2016
f1_keywords:
- C2094
helpviewer_keywords:
- C2094
ms.assetid: 9e4f8f88-f189-46e7-91c9-481bacc7af87
ms.openlocfilehash: 35f67da3259b93eb4ef280d45c8e364df07e9889
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251834"
---
# <a name="compiler-error-c2094"></a>Ошибка компилятора C2094

метка "идентификатор" не определена

Метка, используемая оператором [goto](../../cpp/goto-statement-cpp.md) , не существует в функции.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2094:

```cpp
// C2094.c
int main() {
   goto test;
}   // C2094
```

Возможное решение:

```cpp
// C2094b.c
int main() {
   goto test;
   test:
   {
   }
}
```
