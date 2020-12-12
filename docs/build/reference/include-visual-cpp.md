---
description: 'Дополнительные сведения о: &lt; include&gt;'
title: '&lt;включить> (комментарии к документации по C++)'
ms.date: 11/04/2016
f1_keywords:
- <include>
helpviewer_keywords:
- include C++ XML tag
- <include> C++ XML tag
ms.assetid: 392a3e61-0371-4617-8362-446650876ce3
ms.openlocfilehash: 577281b293fcca9b9b0b9491dd239240d435f32c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199783"
---
# <a name="ltincludegt"></a>&lt;include&gt;

Тег \<include> позволяет задать ссылку на комментарии в другом файле, которые описывают типы и элементы вашего исходного кода. Этот способ является альтернативой размещению комментариев документации непосредственно в файле исходного кода.  Например, можно использовать \<include> для вставки стандартных комментариев, используемых в команде или компании.

## <a name="syntax"></a>Синтаксис

```
<include file='filename' path='tagpath' />
```

#### <a name="parameters"></a>Параметры

*filename*<br/>
Имя файла, содержащего документацию. Имя файла может быть дополнено с указанием пути.  Заключите имя в одинарные или двойные кавычки.  Если компилятору не удается найти `filename`, он выдает предупреждение.

*tagpath*<br/>
Допустимое выражение XPath, которое выбирает нужный набор узлов, содержащийся в файле.

*name*<br/>
Спецификатор имени в теге, предшествующий комментариям. `name` будет иметь идентификатор `id`.

*id*<br/>
Идентификатор тега, который предшествует комментариям.  Заключите имя в одинарные или двойные кавычки.

## <a name="remarks"></a>Комментарии

Тег \<include> использует XML-синтаксис XPath. Способы настройки с помощью см. в документации по XPath \<include> .

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

## <a name="example"></a>Пример

В этом примере представлено несколько файлов. Первый файл, который использует \<include> , содержит следующие комментарии к документации:

```cpp
// xml_include_tag.cpp
// compile with: /clr /doc /LD
// post-build command: xdcmake xml_include_tag.dll

/// <include file='xml_include_tag.doc' path='MyDocs/MyMembers[@name="test"]/*' />
public ref class Test {
   void TestMethod() {
   }
};

/// <include file='xml_include_tag.doc' path='MyDocs/MyMembers[@name="test2"]/*' />
public ref class Test2 {
   void Test() {
   }
};
```

Второй файл (xml_include_tag.doc) содержит следующие комментарии документации:

```xml
<MyDocs>

<MyMembers name="test">
<summary>
The summary for this type.
</summary>
</MyMembers>

<MyMembers name="test2">
<summary>
The summary for this other type.
</summary>
</MyMembers>

</MyDocs>
```

## <a name="program-output"></a>Выходные данные программы

```xml
<?xml version="1.0"?>
<doc>
    <assembly>
        <name>t2</name>
    </assembly>
    <members>
        <member name="T:Test">
            <summary>
The summary for this type.
</summary>
        </member>
        <member name="T:Test2">
            <summary>
The summary for this other type.
</summary>
        </member>
    </members>
</doc>
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
