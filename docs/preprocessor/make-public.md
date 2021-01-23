---
description: Дополнительные сведения об pragma директиве make_public в Microsoft C/C++
title: make_public pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.make_public
- make_public_CPP
helpviewer_keywords:
- pragma, make_public
- make_public pragma
no-loc:
- pragma
ms.openlocfilehash: 4bc3370ac0901ff9a0656de5657f9c9f557e1dff
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713523"
---
# <a name="make_public-no-locpragma"></a>`make_public` pragma

Указывает, что собственный тип должен иметь открытый доступ к сборке.

## <a name="syntax"></a>Синтаксис

> **`#pragma make_public(`***тип***`)`**

### <a name="parameters"></a>Параметры

*type*\
Имя типа, для которого требуется доступность общедоступной сборки.

## <a name="remarks"></a>Примечания

**`make_public`** полезен для, если собственный тип, на который необходимо сослаться, находится в файле заголовка, который нельзя изменить. Если вы хотите использовать собственный тип в сигнатуре открытой функции в типе с видимостью общедоступной сборки, то собственный тип должен также иметь доступность общедоступной сборки, иначе компилятор выдаст предупреждение.

**`make_public`** должен быть указан в глобальной области видимости. Он действует только с точки, в которой он объявлен в конце файла исходного кода.

Собственный тип может быть неявно или явно закрытым. Дополнительные сведения см. в разделе [Visibility Type](../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Type_visibility).

## <a name="examples"></a>Примеры

Следующий пример представляет собой содержимое файла заголовка, содержащего определения двух машинных структур.

```cpp
// make_public_pragma.h
struct Native_Struct_1 { int i; };
struct Native_Struct_2 { int i; };
```

В следующем примере кода используется файл заголовка. Это показывает, что если явно не пометить собственные структуры как открытые с помощью **`make_public`** , компилятор выдаст предупреждение при попытке использовать собственные структуры в сигнатуре открытой функции в общедоступном управляемом типе.

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

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
