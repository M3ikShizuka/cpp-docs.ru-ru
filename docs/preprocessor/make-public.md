---
description: 'Дополнительные сведения о: make_public pragma'
title: Прагма make_public
ms.date: 08/29/2019
f1_keywords:
- vc-pragma.make_public
- make_public_CPP
helpviewer_keywords:
- pragmas, make_public
- make_public pragma
ms.assetid: c3665f4d-268a-4932-9661-c37c8ae6a341
ms.openlocfilehash: 327a9882e13f9c51182e0673443566b56177d320
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333402"
---
# <a name="make_public-pragma"></a>Прагма make_public

Указывает, что собственный тип должен иметь открытый доступ к сборке.

## <a name="syntax"></a>Синтаксис

> **make_public #pragma (** *тип* **)**

### <a name="parameters"></a>Параметры

*type*\
Имя типа, для которого требуется доступность общедоступной сборки.

## <a name="remarks"></a>Комментарии

**make_public** удобно использовать, если собственный тип, на который необходимо сослаться, находится в файле заголовка, который нельзя изменить. Если вы хотите использовать собственный тип в сигнатуре открытой функции в типе с видимостью общедоступной сборки, то собственный тип должен также иметь доступность общедоступной сборки, иначе компилятор выдаст предупреждение.

**make_public** должен быть указан в глобальной области видимости. Он действует только с точки, в которой он объявлен в конце файла исходного кода.

Собственный тип может быть неявно или явно закрытым. Дополнительные сведения см. в разделе [Visibility Type](../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Type_visibility).

## <a name="examples"></a>Примеры

Следующий пример представляет собой содержимое файла заголовка, содержащего определения двух машинных структур.

```cpp
// make_public_pragma.h
struct Native_Struct_1 { int i; };
struct Native_Struct_2 { int i; };
```

В следующем примере кода используется файл заголовка. Это показывает, что если явно не пометить собственные структуры как открытые с помощью **make_public**, компилятор выдаст предупреждение при попытке использовать собственные структуры в сигнатуре открытой функции в общедоступном управляемом типе.

```cpp
// make_public_pragma.cpp
// compile with: /c /clr /W1
#pragma warning (default : 4692)
#include "make_public_pragma.h"
#pragma make_public(Native_Struct_1)

public ref struct A {
   void Test(Native_Struct_1 u) {u.i = 0;}   // OK
   void Test(Native_Struct_2 u) {u.i = 0;}   // C4692
};
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и ключевое слово __pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)
