---
description: 'Дополнительные сведения о: &lt; Примечания&gt;'
title: '&lt;Примечания> (комментарии к документации по C++)'
ms.date: 11/04/2016
f1_keywords:
- <remarks>
helpviewer_keywords:
- <remarks> C++ XML tag
- remarks C++ XML tag
ms.assetid: c820083b-3192-40ab-9ec8-1472c55b4247
ms.openlocfilehash: 3e3590bff827606ad38f3772b72fa4e79563c2e1
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126095"
---
# <a name="ltremarksgt"></a>&lt;remarks&gt;

Тег \<remarks> позволяет добавить сведения о типе, дополняющие информацию, указанную с помощью тега [\<summary>](summary-visual-cpp.md). Эта информация отображается в [обозревателе объектов](/visualstudio/ide/viewing-the-structure-of-code) и в веб-отчете комментариев кода.

## <a name="syntax"></a>Синтаксис

```
<remarks>description</remarks>
```

#### <a name="parameters"></a>Параметры

*description*<br/>
Описание элемента.

## <a name="remarks"></a>Примечания

Скомпилируйте с [/doc](doc-process-documentation-comments-c-cpp.md) для обработки комментариев документации в файл.

## <a name="example"></a>Пример

```cpp
// xml_remarks_tag.cpp
// compile with: /LD /clr /doc
// post-build command: xdcmake xml_remarks_tag.dll

using namespace System;

/// <summary>
/// You may have some primary information about this class.
/// </summary>
/// <remarks>
/// You may have some additional information about this class.
/// </remarks>
public ref class MyClass {};
```

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
