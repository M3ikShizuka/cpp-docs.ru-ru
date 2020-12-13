---
description: 'Дополнительные сведения о: Ошибка компилятора C2464'
title: Ошибка компилятора C2464
ms.date: 11/04/2016
f1_keywords:
- C2464
helpviewer_keywords:
- C2464
ms.assetid: ace953d6-b414-49ee-bfef-90578a8da00c
ms.openlocfilehash: 2e30166529616809478927dbfe6ff1f1efb3002a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341845"
---
# <a name="compiler-error-c2464"></a>Ошибка компилятора C2464

"идентификатор": невозможно использовать "New" для выделения ссылки

Идентификатор ссылки был выделен **`new`** оператором. Ссылки не являются объектами памяти, поэтому **`new`** не могут возвращать указатель на них. Используйте синтаксис объявления стандартной переменной для объявления ссылки.

Следующий пример приводит к возникновению ошибки C2464:

```cpp
// C2464.cpp
int main() {
   new ( int& ir );   // C2464
}
```
