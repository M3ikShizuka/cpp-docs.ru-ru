---
description: 'Дополнительные сведения о: Ошибка компилятора C2045'
title: Ошибка компилятора C2045
ms.date: 11/04/2016
f1_keywords:
- C2045
helpviewer_keywords:
- C2045
ms.assetid: 2fca668e-9b20-4933-987a-18c0fd0187df
ms.openlocfilehash: 878ae18a20bbaa0da7219e2a68f8772c5dd0a637
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175174"
---
# <a name="compiler-error-c2045"></a>Ошибка компилятора C2045

"идентификатор": переопределение метки

Метка стоит перед несколькими операторами в одной функции.

В следующем примере возникает ошибка C2045.

```cpp
// C2045.cpp
int main() {
   label: {
   }
   goto label;
   label: {}   // C2045
}
```
