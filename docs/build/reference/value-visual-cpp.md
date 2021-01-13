---
description: 'Дополнительные сведения: &lt; значение&gt;'
title: '&lt;> значений (комментарии к документации по C++)'
ms.date: 11/04/2016
f1_keywords:
- <value>
helpviewer_keywords:
- value C++ XML tag
- <value> C++ XML tag
ms.assetid: 0ba0a0d5-bcd7-4862-a169-83f2721ad80e
ms.openlocfilehash: 5ebab554a33ff0d90b9306f3aec56b2552e18c5a
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126329"
---
# <a name="ltvaluegt"></a>&lt;value&gt;

\<value>Тег позволяет описать методы доступа свойств и свойств. Обратите внимание, что при добавлении свойства с помощью мастера кода в интегрированной среде разработки Visual Studio будет добавлен [\<summary>](summary-visual-cpp.md) тег для нового свойства. После этого следует вручную добавить тег \<value> для описания значения, которое представляется свойством.

## <a name="syntax"></a>Синтаксис

```
<value>property-description</value>
```

#### <a name="parameters"></a>Параметры

*property-description*<br/>
Описание свойства.

## <a name="remarks"></a>Примечания

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

## <a name="example"></a>Пример

```cpp
// xml_value_tag.cpp
// compile with: /LD /clr /doc
// post-build command: xdcmake xml_value_tag.dll
using namespace System;
/// Text for class Employee.
public ref class Employee {
private:
   String ^ name;
   /// <value>Name accesses the value of the name data member</value>
public:
   property String ^ Name {
      String ^ get() {
         return name;
      }
      void set(String ^ i) {
         name = i;
      }
   }
};
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
