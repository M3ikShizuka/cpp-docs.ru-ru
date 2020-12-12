---
description: 'Дополнительные сведения: async_uuid'
title: async_uuid (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.async_uuid
helpviewer_keywords:
- async_uuid attribute
ms.assetid: 235cb0d7-be58-4dd9-983c-e2a21bbc42c6
ms.openlocfilehash: cb55fe66f05bfc7879470bfa6c64c00ffd2913e8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97205334"
---
# <a name="async_uuid"></a>async_uuid

Указывает UUID, который направляет компилятор MIDL для определения синхронных и асинхронных версий COM-интерфейса.

## <a name="syntax"></a>Синтаксис

```cpp
[async_uuid (uuid)]
```

### <a name="parameters"></a>Параметры

*uuid*<br/>
UUID, определяющий версию интерфейса.

## <a name="remarks"></a>Комментарии

Атрибут **async_uuid** C++ имеет те же функциональные возможности, что и атрибут [async_uuid](/windows/win32/Midl/async-uuid) MIDL.

## <a name="example"></a>Пример

```cpp
// cpp_attr_ref_async_uuid.cpp
// compile with: /LD
#include <Windows.h>
[module(name="Test")];
[object, uuid("9e66a290-4365-11d2-a997-00c04fa37ddb"),
async_uuid("e8583106-38fd-487e-912e-4fc8645c677e")]
__interface ICustom {
   HRESULT Custom([in] long l, [out, retval] long *pLong);
};
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|`interface`|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|**Dual**, **DISP**|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты интерфейса](interface-attributes.md)
