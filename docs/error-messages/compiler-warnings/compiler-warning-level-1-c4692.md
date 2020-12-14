---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4692'
title: Предупреждение компилятора (уровень 1) C4692
ms.date: 11/04/2016
f1_keywords:
- C4692
helpviewer_keywords:
- C4692
ms.assetid: f6fb3acc-8228-491a-9c30-ce302d8a9c75
ms.openlocfilehash: 7c38a2bd4bfd4de943f64483cd8a9e96ece0b580
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97249130"
---
# <a name="compiler-warning-level-1-c4692"></a>Предупреждение компилятора (уровень 1) C4692

"функция": подпись не частного члена содержит частный собственный тип сборки "частныйТип"

Тип, видимый за пределами сборки, содержит функцию-член, сигнатура которой содержит собственный тип, невидимый за пределами сборки. Поэтому функция-член не должна вызываться, если экземпляр содержащего его типа создается вне сборки.

Дополнительные сведения см. в разделе [Visibility Type](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Type_visibility).

Это предупреждение отключено по умолчанию. Дополнительные сведения см. в разделе [Compiler Warnings That Are Off by Default](../../preprocessor/compiler-warnings-that-are-off-by-default.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4692.

```cpp
// C4692.cpp
// compile with: /W1 /c /clr
#pragma warning(default:4692)
class Private_Native_Class {};
public class Public_Native_Class {};
public ref class Public_Ref_Class {
public:
   void Test(Private_Native_Class *) {}   // C4692
   void Test2(Public_Native_Class *) {}   // OK
};
```
