---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4258'
title: Предупреждение компилятора (уровень 1) C4258
ms.date: 11/04/2016
f1_keywords:
- C4258
helpviewer_keywords:
- C4258
ms.assetid: bbb75e6d-6693-4e62-8ed3-b006a0ec55e3
ms.openlocfilehash: 1a9bf1fdb6bded2bfad76f25c8bd1bbeadd43bf7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97266212"
---
# <a name="compiler-warning-level-1-c4258"></a>Предупреждение компилятора (уровень 1) C4258

"переменная": определение из цикла for игнорируется; используется определение из включающей области "

В параметрах [/Ze](../../build/reference/za-ze-disable-language-extensions.md) и [/Zc: forScope](../../build/reference/zc-forscope-force-conformance-in-for-loop-scope.md)переменные, определенные в цикле [for](../../cpp/for-statement-cpp.md) , выходят за пределы области действия после **`for`** завершения цикла. Это предупреждение возникает, если переменная с тем же именем, что и у переменной цикла, но определена во внешнем цикле, снова используется в области, содержащей **`for`** цикл. Пример:

```cpp
// C4258.cpp
// compile with: /Zc:forScope /W1
int main()
{
   int i;
   {
      for (int i =0; i < 1; i++)
         ;
      i = 20;   // C4258 i (in for loop) has gone out of scope
   }
}
```
