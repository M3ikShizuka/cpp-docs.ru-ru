---
description: 'Дополнительные сведения: &lt; тег Exception &gt;'
title: '&lt;> исключений (комментарии к документации по C++)'
ms.date: 11/04/2016
helpviewer_keywords:
- <exception> C++ XML tag
- exception C++ XML tag
ms.assetid: 24451e79-9b89-4b77-98fb-702c6516b818
ms.openlocfilehash: c75f2a4a10386664e23b5ba730e1827c6d74af71
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192425"
---
# <a name="ltexceptiongt-tag"></a>&lt;&gt;тег исключения

Тег \<exception> служит для указания возможных исключений. Этот тег применяется к определению метода.

## <a name="syntax"></a>Синтаксис

```
<exception cref="member">description</exception>
```

#### <a name="parameters"></a>Параметры

*участниками*<br/>
Ссылка на исключение, которое доступно из текущей среды компиляции. Используя правила подстановки имен, компилятор проверяет, существует ли исключение, и приводит `member` к каноническому имени элемента в выходных XML-данных.  Если компилятору не удается найти `member`, он выдает предупреждение.

Заключите имя в одинарные или двойные кавычки.

Сведения о том, как создать ссылку cref на универсальный тип, см. в разделе [\<see>](see-visual-cpp.md) .

*description*<br/>
Описание.

## <a name="remarks"></a>Комментарии

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

Компилятор КОМПИЛЯТОРОМ MSVC будет пытаться разрешить ссылки cref в одном проходе через комментарии к документации.  Поэтому если при использовании правил поиска C++ компилятор не найдет символ, ссылка будет помечена как не разрешенная. [\<seealso>](seealso-visual-cpp.md)Дополнительные сведения см. в разделе.

## <a name="example"></a>Пример

```cpp
// xml_exception_tag.cpp
// compile with: /clr /doc /LD
// post-build command: xdcmake xml_exception_tag.dll
using namespace System;

/// Text for class EClass.
public ref class EClass : public Exception {
   // class definition ...
};

/// <exception cref="System.Exception">Thrown when... .</exception>
public ref class TestClass {
   void Test() {
      try {
      }
      catch(EClass^) {
      }
   }
};
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
