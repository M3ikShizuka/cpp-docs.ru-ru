---
title: '&lt;> paramref (комментарии к документации по C++)'
description: Подробнее о теге XML-документации paramref C++.
ms.date: 11/04/2016
f1_keywords:
- <paramref>
helpviewer_keywords:
- paramref C++ XML tag
- <paramref> C++ XML tag
ms.assetid: c5730dc2-7159-421f-b2d5-bb971e307122
ms.openlocfilehash: 393703e7816368fb80f71d962dc190a0db1cea03
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126160"
---
# <a name="ltparamrefgt"></a>&lt;paramref&gt;

\<paramref>Тег дает возможность указать, что слово является параметром. В XML-файле этот параметр может выделяться особым образом.

## <a name="syntax"></a>Синтаксис

```
<paramref name="name"/>
```

#### <a name="parameters"></a>Параметры

*name*<br/>
Имя параметра, на который указывается ссылка.  Заключите имя в одинарные или двойные кавычки.  Если компилятору не удается найти `name`, он выдает предупреждение.

## <a name="remarks"></a>Remarks

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

## <a name="example"></a>Пример

```cpp
// xml_paramref_tag.cpp
// compile with: /clr /doc /LD
// post-build command: xdcmake xml_paramref_tag.dll
/// Text for class MyClass.
public ref class MyClass {
   /// <summary>MyMethod is a method in the MyClass class.
   /// The <paramref name="Int1"/> parameter takes a number.
   /// </summary>
   void MyMethod(int Int1) {}
};
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
