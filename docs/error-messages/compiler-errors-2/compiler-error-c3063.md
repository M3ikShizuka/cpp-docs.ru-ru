---
description: 'Дополнительные сведения о: Ошибка компилятора C3063'
title: Ошибка компилятора C3063
ms.date: 11/04/2016
f1_keywords:
- C3063
helpviewer_keywords:
- C3063
ms.assetid: 0ecf6f1f-e4a7-487a-9fd5-79d8ac470001
ms.openlocfilehash: 304359e34b6cbae07d2f901db02c6e5ed04e373c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97281708"
---
# <a name="compiler-error-c3063"></a>Ошибка компилятора C3063

оператор "operator": все операнды должны иметь одинаковый тип перечисления

При использовании операторов в перечислителях оба операнда должны иметь тип перечисления. Дополнительные сведения см. [в разделе инструкции. Определение и использование перечислений в C++/CLI](../../dotnet/how-to-define-and-consume-enums-in-cpp-cli.md).

## <a name="example"></a>Пример

В следующем примере создается C3063 и демонстрируется его устранение.

```cpp
// C3063.cpp
// compile with: /clr
enum class E { a, b } e, mask;
int main() {
   if ( ( e & mask ) != 0 ) ;   // C3063 no operator!= (E, int)

   if ( ( e & mask ) != E() )   // OK
      ;
}
```
