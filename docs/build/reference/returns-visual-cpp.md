---
description: 'Дополнительные сведения: &lt; возвращает&gt;'
title: '&lt;Возвращает> (комментарии к документации по C++)'
ms.date: 11/04/2016
f1_keywords:
- <returns>
helpviewer_keywords:
- returns C++ XML tag
- <returns> C++ XML tag
ms.assetid: 5e3b0ed9-838d-4953-a93e-76d2d0a19fb9
ms.openlocfilehash: 59b9a7d33a3b2695a2a5e22fdac465f17c915492
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126121"
---
# <a name="ltreturnsgt"></a>&lt;returns&gt;

Тег \<returns> следует использовать в комментариях к объявлению метода для описания возвращаемого значения.

## <a name="syntax"></a>Синтаксис

```
<returns>description</returns>
```

#### <a name="parameters"></a>Параметры

*description*<br/>
Описание возвращаемого значения.

## <a name="remarks"></a>Примечания

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

## <a name="example"></a>Пример

```cpp
// xml_returns_tag.cpp
// compile with: /LD /clr /doc
// post-build command: xdcmake xml_returns_tag.dll

/// Text for class MyClass.
public ref class MyClass {
public:
   /// <returns>Returns zero.</returns>
   int GetZero() { return 0; }
};
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
