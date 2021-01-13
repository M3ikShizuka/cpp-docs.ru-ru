---
description: 'Дополнительные сведения: &lt; пример&gt;'
title: '&lt;Пример> (комментарии к документации по C++)'
ms.date: 11/04/2016
f1_keywords:
- <example>
helpviewer_keywords:
- <example> C++ XML tag
- example C++ XML tag
ms.assetid: c821aaa7-7ea7-4bee-9922-6705ad57f877
ms.openlocfilehash: 61624efd34c02d75c7109a3211914b2018c513ae
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98125887"
---
# <a name="ltexamplegt"></a>&lt;example&gt;

Тег \<example> позволяет указать пример использования метода или другого элемента библиотеки. Как правило, это также подразумевает использование [\<code>](code-visual-cpp.md) тега.

## <a name="syntax"></a>Синтаксис

```
<example>description</example>
```

#### <a name="parameters"></a>Параметры

*description*<br/>
Описание примера кода.

## <a name="remarks"></a>Примечания

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

## <a name="example"></a>Пример

```cpp
// xml_example_tag.cpp
// compile with: /clr /doc /LD
// post-build command: xdcmake xml_example_tag.dll

/// Text for class MyClass.
public ref class MyClass {
public:
   /// <summary>
   /// GetZero method
   /// </summary>
   /// <example> This sample shows how to call the GetZero method.
   /// <code>
   /// int main()
   /// {
   ///    return GetZero();
   /// }
   /// </code>
   /// </example>
   static int GetZero() {
      return 0;
   }
};
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
