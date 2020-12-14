---
description: 'Подробнее: глобальные константы в C++'
title: Глобальные константы в C++
ms.date: 11/04/2016
helpviewer_keywords:
- global constants
- constants, global
ms.assetid: df5a9bd4-d0a8-4c1c-956e-b481d0bded7d
ms.openlocfilehash: 8e960e7e10942fc231fcdeafef6e8d755694c460
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97261662"
---
# <a name="global-constants-in-c"></a>Глобальные константы в C++

Глобальные константы C++ имеют статическую компоновку. Это отличается от C. При попытке использовать глобальную константу в C++ в нескольких файлах вы получаете неразрешенную внешнюю ошибку. Компилятор оптимизирует глобальные константы, не освобождая пространство, зарезервированное для переменной.

Одним из способов устранения этой ошибки является включение инициализации констант в файл заголовка и включение этого заголовка в CPP-файлы при необходимости, точно так же, как если бы он был прототипом функции. Другая возможность — сделать переменную неконстантной и использовать постоянную ссылку при оценке.

Следующий пример приводит к возникновению ошибки C2019:

```cpp
// global_constants.cpp
// LNK2019 expected
void test(void);
const int lnktest1 = 0;

int main() {
   test();
}
```

Затем:

```cpp
// global_constants_2.cpp
// compile with: global_constants.cpp
extern int lnktest1;

void test() {
  int i = lnktest1;   // LNK2019
}
```

## <a name="see-also"></a>См. также раздел

[Ошибка средств компоновщика LNK2019](../../error-messages/tool-errors/linker-tools-error-lnk2019.md)
