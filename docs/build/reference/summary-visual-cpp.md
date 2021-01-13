---
description: 'Дополнительные сведения: &lt; Сводка&gt;'
title: '&lt;> сводки (комментарии к документации по C++)'
ms.date: 11/04/2016
f1_keywords:
- <summary>
helpviewer_keywords:
- <summary> C++ XML tag
- summary C++ XML tag
ms.assetid: cdeeefbb-1339-45d6-9002-10042a9a2726
ms.openlocfilehash: 3003a3226a67d864be1a07a47151e7003c5514a4
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126342"
---
# <a name="ltsummarygt"></a>&lt;summary&gt;

Тег \<summary> следует использовать для описания типа или элемента типа. Чтобы добавить дополнительную информацию в описание типа, используйте [\<remarks>](remarks-visual-cpp.md).

## <a name="syntax"></a>Синтаксис

```
<summary>description</summary>
```

#### <a name="parameters"></a>Параметры

*description*<br/>
Сводка объекта.

## <a name="remarks"></a>Примечания

Текст для \<summary> тега — единственный источник сведений о типе в IntelliSense, который также отображается в [обозревателе объектов](/visualstudio/ide/viewing-the-structure-of-code) и в веб-отчете с комментариями кода.

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

## <a name="example"></a>Пример

```cpp
// xml_summary_tag.cpp
// compile with: /LD /clr /doc
// post-build command: xdcmake xml_summary_tag.dll

/// Text for class MyClass.
public ref class MyClass {
public:
   /// <summary>MyMethod is a method in the MyClass class.
   /// <para>Here's how you could make a second paragraph in a description. <see cref="System::Console::WriteLine"/> for information about output statements.</para>
   /// <seealso cref="MyClass::MyMethod2"/>
   /// </summary>
   void MyMethod(int Int1) {}

   /// text
   void MyMethod2() {}
};
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
