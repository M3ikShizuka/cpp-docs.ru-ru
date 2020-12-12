---
description: 'Дополнительные сведения о: Ошибка компилятора C3099'
title: Ошибка компилятора C3099
ms.date: 11/04/2016
f1_keywords:
- C3099
helpviewer_keywords:
- C3099
ms.assetid: b3dded0f-76c9-42c1-991b-532eb8619661
ms.openlocfilehash: d065edd58df1e9196dc6aa31cfd4fb263f062f1d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97116227"
---
# <a name="compiler-error-c3099"></a>Ошибка компилятора C3099

keyword: используйте [System::AttributeUsageAttribute] для управляемых атрибутов; используйте [Windows::Foundation::Metadata::AttributeUsageAttribute] для атрибутов WinRT

Используйте <xref:System.AttributeUsageAttribute> для объявления атрибутов **/CLR** . Используйте `Windows::Foundation::Metadata::AttributeUsageAttribute` для объявления атрибутов среды выполнения Windows.

Дополнительные сведения об атрибутах/CLR см. в разделе [определяемые пользователем атрибуты](../../extensions/user-defined-attributes-cpp-component-extensions.md). Поддерживаемые атрибуты в среда выполнения Windows см. в разделе [пространство имен Windows. Foundation. Metadata.](/uwp/api/windows.foundation.metadata)

## <a name="example"></a>Пример

В следующем примере показано возникновение ошибки C3099 и приводятся сведения по ее устранению.

```cpp
// C3099.cpp
// compile with: /clr /c
using namespace System;
[usage(10)]   // C3099
// try the following line instead
// [AttributeUsageAttribute(AttributeTargets::All)]
ref class A : Attribute {};
```
