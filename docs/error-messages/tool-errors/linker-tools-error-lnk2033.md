---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK2033'
title: Ошибка средств компоновщика LNK2033
ms.date: 11/04/2016
f1_keywords:
- LNK2033
helpviewer_keywords:
- LNK2033
ms.assetid: d61db467-9328-4788-bf54-e2a20537f13f
ms.openlocfilehash: 46ee94e0aff4379a6d28a508ed1394e90ef9a96d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97275650"
---
# <a name="linker-tools-error-lnk2033"></a>Ошибка средств компоновщика LNK2033

Неразрешенная лексема typeref (токен) для "тип"

Тип не имеет определения в метаданных MSIL.

LNK2033 может возникать при компиляции с **параметром/clr: Сейф** и при наличии только прямого объявления для типа в модуле MSIL, где в модуле MSIL имеется ссылка на тип.

Тип должен быть определен в **параметре/CLR: Сейф**.

Дополнительные сведения см. в разделе [/CLR (компиляция среды CLR)](../../build/reference/clr-common-language-runtime-compilation.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки LNK2033.

```cpp
// LNK2033.cpp
// compile with: /clr:safe
// LNK2033 expected
ref class A;
ref class B {};

int main() {
   A ^ aa = nullptr;
   B ^ bb = nullptr;   // OK
};
```
