---
description: 'Дополнительные сведения: &lt; разрешение&gt;'
title: '&lt;> разрешений (комментарии к документации по C++)'
ms.date: 11/04/2016
f1_keywords:
- <permission>
helpviewer_keywords:
- <permission> C++ XML tag
- permission C++ XML tag
ms.assetid: 537ee2bc-95bd-48e4-9ce6-3420c3da87f4
ms.openlocfilehash: faade1711afa1f086d26104242dbdb3cb8814462
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126108"
---
# <a name="ltpermissiongt"></a>&lt;permission&gt;

Тег \<permission> позволяет документировать уровень доступа для элемента. <xref:System.Security.PermissionSet> позволяет задать уровень доступа для члена.

## <a name="syntax"></a>Синтаксис

```
<permission cref="member">description</permission>
```

#### <a name="parameters"></a>Параметры

*участниками*<br/>
Ссылка на член или поле, которые доступны для вызова из текущей среды компиляции. Компилятор проверяет, существует ли элемент кода, и приводит `member` к каноническому имени элемента в выходных XML-данных.  Заключите имя в одинарные или двойные кавычки.

Если компилятору не удается найти `member`, он выдает предупреждение.

Сведения о том, как создать ссылку cref на универсальный тип, см. в разделе [\<see>](see-visual-cpp.md) .

*description*<br/>
Описание уровня доступа для члена.

## <a name="remarks"></a>Примечания

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

Компилятор КОМПИЛЯТОРОМ MSVC будет пытаться разрешить ссылки cref в одном проходе через комментарии к документации.  Поэтому если при использовании правил поиска C++ компилятор не найдет символ, ссылка будет помечена как не разрешенная. [\<seealso>](seealso-visual-cpp.md)Дополнительные сведения см. в разделе.

## <a name="example"></a>Пример

```cpp
// xml_permission_tag.cpp
// compile with: /clr /doc /LD
// post-build command: xdcmake xml_permission_tag.dll
using namespace System;
/// Text for class TestClass.
public ref class TestClass {
   /// <permission cref="System::Security::PermissionSet">Everyone can access this method.</permission>
   void Test() {}
};
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
