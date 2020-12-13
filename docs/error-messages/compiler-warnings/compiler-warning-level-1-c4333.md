---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4333'
title: Предупреждение компилятора (уровень 1) C4333
ms.date: 11/04/2016
f1_keywords:
- C4333
helpviewer_keywords:
- C4333
ms.assetid: d3763c52-6110-4da0-84db-5264e3f3f166
ms.openlocfilehash: 7a9384ad9dad8b17e6541256c71d28066d557df5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340041"
---
# <a name="compiler-warning-level-1-c4333"></a>Предупреждение компилятора (уровень 1) C4333

"оператор": слишком большое смещение вправо, потери данных

Операция сдвига вправо слишком велика.  Все значащие биты сдвигаются, и результат всегда будет равен нулю.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4333.

```cpp
// C4333.cpp
// compile with: /c /W1
unsigned shift8 (unsigned char c) {
   return c >> 8;   // C4333

   // try the following line instead
   // return c >> 4;   // OK
}
```
