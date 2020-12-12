---
description: 'Дополнительные сведения о: Ошибка компилятора C2434'
title: Ошибка компилятора C2434
ms.date: 11/04/2016
f1_keywords:
- C2434
helpviewer_keywords:
- C2434
ms.assetid: 01329e26-7c74-4219-b74f-69e3a40c9738
ms.openlocfilehash: e24eb3fdf2ae60dadc270bed1bdda251acfc70a3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97189968"
---
# <a name="compiler-error-c2434"></a>Ошибка компилятора C2434

> "*символ*": символ, объявленный с __declspec (Process), не может быть динамически инициализирован в режиме/clr: pure

## <a name="remarks"></a>Комментарии

Параметры компилятора **/clr: pure** и **/clr: Сейф** являются устаревшими в Visual Studio 2015 и не поддерживаются в Visual Studio 2017.

Невозможно динамически инициализировать переменную для каждого процесса в **параметре/CLR: pure**. Дополнительные сведения см. в разделе [/CLR (компиляция среды CLR)](../../build/reference/clr-common-language-runtime-compilation.md) и [Обработка](../../cpp/process.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2434. Чтобы устранить эту проблему, используйте константы для инициализации `process` переменных.

```cpp
// C2434.cpp
// compile with: /clr:pure /c
int f() { return 0; }
__declspec(process) int i = f();   // C2434
__declspec(process) int i2 = 0;   // OK
```
