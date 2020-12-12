---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4792'
title: Предупреждение компилятора (уровень 3) C4792
ms.date: 11/04/2016
f1_keywords:
- C4792
helpviewer_keywords:
- C4792
ms.assetid: c047ce69-a622-44e1-9425-d41aa9261c61
ms.openlocfilehash: 37dc805477e3150eedaffe7eb5d900b7903b1d48
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332127"
---
# <a name="compiler-warning-level-3-c4792"></a>Предупреждение компилятора (уровень 3) C4792

на функцию "функция", объявленную с использованием sysimport, ссылается машинный код; импортируйте библиотеку, необходимую для компоновки

Собственная функция, импортированная в программу с помощью DllImport, вызывается из неуправляемой функции. Таким образом, необходимо привязать библиотеку импорта для библиотеки DLL.

Это предупреждение нельзя разрешить в коде или путем изменения способа компиляции. Используйте прагму [warning](../../preprocessor/warning.md) , чтобы отключить это предупреждение.

В следующем примере возникает ошибка C4792:

```cpp
// C4792.cpp
// compile with: /clr /W3
// C4792 expected
using namespace System::Runtime::InteropServices;
[DllImport("msvcrt")]
extern "C" int __cdecl puts(const char *);
int main() {}

// Uncomment the following line to resolve.
// #pragma warning(disable : 4792)
#pragma unmanaged
void func(void){
   puts("test");
}
```
