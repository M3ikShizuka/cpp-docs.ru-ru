---
description: 'Дополнительные сведения о: Ошибка компилятора C2812'
title: Ошибка компилятора C2812
ms.date: 11/04/2016
f1_keywords:
- C2812
helpviewer_keywords:
- C2812
ms.assetid: 22aadb8c-7232-489d-a3ad-60662dda30a8
ms.openlocfilehash: d59105397ae773c2a46b04a64eb50da3055c3a4b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97278430"
---
# <a name="compiler-error-c2812"></a>Ошибка компилятора C2812

> \#Импорт не поддерживается с параметрами/clr: pure и/CLR: Сейф

## <a name="remarks"></a>Комментарии

Параметры компилятора **/clr: pure** и **/clr: Сейф** являются устаревшими в Visual Studio 2015 и не поддерживаются в Visual Studio 2017.

[директива #import](../../preprocessor/hash-import-directive-cpp.md) не поддерживается с **параметрами/clr: pure** и **/clr: Сейф** , так как `#import` требует использования библиотек поддержки собственного компилятора.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2812.

```cpp
// C2812.cpp
// compile with: /clr:pure /c
#import "importlib.tlb"   // C2812
```
