---
description: 'Дополнительные сведения: &lt; возвращает&gt;'
title: '&lt;Возвращает> (комментарии к документации по C++)'
ms.date: 11/04/2016
f1_keywords:
- returns
- <returns>
helpviewer_keywords:
- returns C++ XML tag
- <returns> C++ XML tag
ms.assetid: 5e3b0ed9-838d-4953-a93e-76d2d0a19fb9
ms.openlocfilehash: c07439610fa0259a38a4c1993ead7f0f06023e5e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225054"
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
