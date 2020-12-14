---
description: 'Дополнительные сведения о: предупреждение компилятора C4936'
title: Предупреждение компилятора C4936
ms.date: 11/04/2016
f1_keywords:
- C4936
helpviewer_keywords:
- C4936
ms.assetid: 6676de35-bf1b-4d0b-a70f-b5734130336c
ms.openlocfilehash: e12cb789d3d008ec61672591cde78f1b7dc61da6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314988"
---
# <a name="compiler-warning-c4936"></a>Предупреждение компилятора C4936

> Данный __declspec поддерживается только при компиляции с параметрами /clr или /clr:pure

## <a name="remarks"></a>Комментарии

Параметр компилятора **/clr: pure** является устаревшим в visual Studio 2015 и не поддерживается в visual Studio 2017.

**`__declspec`** Использован модификатор, но этот **`__declspec`** Модификатор допустим только при компиляции с одним из параметров [/CLR](../../build/reference/clr-common-language-runtime-compilation.md) .

Дополнительные сведения см. в разделах [appdomain](../../cpp/appdomain.md) и [process](../../cpp/process.md).

C4936 всегда выдается как ошибка.  Вы можете отключить C4936 с помощью директивы [warning](../../preprocessor/warning.md) .

## <a name="example"></a>Пример

При компиляции следующего примера возникнет ошибка C4936:

```cpp
// C4936.cpp
// compile with: /c
// #pragma warning (disable : 4936)
__declspec(process) int i;   // C4936
__declspec(appdomain) int j;   // C4936
```
