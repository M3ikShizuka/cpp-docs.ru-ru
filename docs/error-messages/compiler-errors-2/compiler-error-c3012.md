---
description: 'Дополнительные сведения о: Ошибка компилятора C3012'
title: Ошибка компилятора C3012
ms.date: 11/04/2016
f1_keywords:
- C3012
helpviewer_keywords:
- C3012
ms.assetid: cc7040b1-b3fb-4da6-a474-877914d30332
ms.openlocfilehash: fff986a984acb62f770d02ff2b7b08c40e8511e3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286011"
---
# <a name="compiler-error-c3012"></a>Ошибка компилятора C3012

> "*внутренний*": встроенная функция не разрешена непосредственно в параллельной области

[Встроенная функция компилятора](../../intrinsics/compiler-intrinsics.md) не может находиться в области `omp parallel` . Чтобы устранить эту проблему, переместите внутренние объекты из региона или замените их невстроенными эквивалентами.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3012 и демонстрирует один из способов его исправления:

```cpp
// C3012.cpp
// compile with: /openmp
#ifdef __cplusplus
extern "C" {
#endif
void* _ReturnAddress();
#ifdef __cplusplus
}
#endif

int main()
{
   #pragma omp parallel
   {
      _ReturnAddress();   // C3012
   }
   _ReturnAddress();      // OK
}
```
