---
description: 'Дополнительные сведения о: Ошибка компилятора C2261'
title: Ошибка компилятора C2261
ms.date: 11/04/2016
f1_keywords:
- C2261
helpviewer_keywords:
- C2261
ms.assetid: 60969482-9e83-49b5-9631-a04bc844da12
ms.openlocfilehash: c5156a240696f9021613b54cf7013e9372a13b45
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134619"
---
# <a name="compiler-error-c2261"></a>Ошибка компилятора C2261

"строка": ссылка на сборку недопустима и не может быть разрешена

Недопустимое значение.

<xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> используется для указания дружественной сборки. Например, если a.dll хочет указать b.dll в качестве дружественной сборки, укажите (в a.dll): InternalsVisibleTo ("b"). Затем среда выполнения позволяет b.dll получить доступ ко всем a.dll (за исключением закрытых типов).

Дополнительные сведения о правильном синтаксисе при указании дружественных сборок см. в разделе [дружественные сборки (C++)](../../dotnet/friend-assemblies-cpp.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2261.

```cpp
// C2261.cpp
// compile with: /clr /c
using namespace System::Runtime::CompilerServices;
[assembly: InternalsVisibleTo("a,a,a")];   // C2261
[assembly: InternalsVisibleTo("a.a")];   // OK
[assembly: InternalsVisibleTo("a")];   // OK
```
