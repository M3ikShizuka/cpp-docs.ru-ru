---
description: 'Дополнительные сведения о: Ошибка компилятора C2472'
title: Ошибка компилятора C2472
ms.date: 11/04/2016
f1_keywords:
- C2472
helpviewer_keywords:
- C2472
ms.assetid: 3b36bcdc-2ba5-4357-ab88-7545ba0551cd
ms.openlocfilehash: a1d4d668c1e7151771a2df85e888384c6c3ea028
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97164501"
---
# <a name="compiler-error-c2472"></a>Ошибка компилятора C2472

> "*функция*" не может быть создана в управляемом коде: "*Message*"; Компиляция с параметром/CLR для создания смешанного образа

## <a name="remarks"></a>Комментарии

Эта ошибка возникает при использовании типов, не поддерживаемых в управляемом коде, в чистой среде CLR. Для устранения этой ошибки выполните компиляцию с параметром **/clr** .

Параметры компилятора **/clr: pure** и **/clr: Сейф** являются устаревшими в Visual Studio 2015 и не поддерживаются в Visual Studio 2017.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2472:

```cpp
// C2472.cpp
// compile with: /clr:pure
// C2472 expected

#include <cstdlib>

int main()
{
   int * __ptr32 p32;
   int * __ptr64 p64;

   p32 = (int * __ptr32)malloc(4);
   p64 = p32;
}
```

## <a name="see-also"></a>См. также раздел

- [/clr (компиляция среды выполнения)](../../build/reference/clr-common-language-runtime-compilation.md)
