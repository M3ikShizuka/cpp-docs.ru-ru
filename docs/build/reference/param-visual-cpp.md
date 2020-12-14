---
description: 'Дополнительные сведения: &lt; param&gt;'
title: '&lt;> param (комментарии к документации по C++)'
ms.date: 11/04/2016
f1_keywords:
- param
- <param>
helpviewer_keywords:
- param C++ XML tag
- <param> C++ XML tag
ms.assetid: 66c1a1c3-4f98-4bcf-8c7d-9a40308982fb
ms.openlocfilehash: 7c3baabc6aef9a4cabdd7c7a9023fb628bd53793
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226146"
---
# <a name="ltparamgt"></a>&lt;param&gt;

Тег \<param> следует использовать в комментариях к объявлению метода для описания одного из параметров такого метода.

## <a name="syntax"></a>Синтаксис

```
<param name='name'>description</param>
```

#### <a name="parameters"></a>Параметры

*name*<br/>
Имя параметра метода.  Заключите имя в одинарные или двойные кавычки.  Если компилятору не удается найти `name`, он выдает предупреждение.

*description*<br/>
Описание параметра.

## <a name="remarks"></a>Примечания

Текст \<param> тега будет отображаться в IntelliSense, в [обозревателе объектов](/visualstudio/ide/viewing-the-structure-of-code)и в веб-отчете с комментариями к коду.

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

## <a name="example"></a>Пример

```cpp
// xml_param_tag.cpp
// compile with: /clr /doc /LD
// post-build command: xdcmake xml_param_tag.dll
/// Text for class MyClass.
public ref class MyClass {
   /// <param name="Int1">Used to indicate status.</param>
   void MyMethod(int Int1) {
   }
};
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
