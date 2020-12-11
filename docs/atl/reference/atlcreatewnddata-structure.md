---
description: 'Дополнительные сведения: структура _AtlCreateWndData'
title: Структура _AtlCreateWndData
ms.date: 11/04/2016
f1_keywords:
- ATL::_AtlCreateWndData
- ATL._AtlCreateWndData
- _AtlCreateWndData
helpviewer_keywords:
- _AtlCreateWndData structure
- AtlCreateWndData structure
ms.assetid: 76ed5382-bfbf-4b8b-8a29-912688dfd2ae
ms.openlocfilehash: 912f2d108baa9cae1b91a34f3c5e386339d11f0b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158612"
---
# <a name="_atlcreatewnddata-structure"></a>Структура _AtlCreateWndData

Эта структура содержит данные экземпляра класса в коде окна в ATL.

## <a name="syntax"></a>Синтаксис

```cpp
    struct _AtlCreateWndData{
    void* m_pThis;
    DWORD m_dwThreadID;
    _AtlCreateWndData* m_pNext;
};
```

## <a name="members"></a>Члены

`m_pThis`<br/>
**`this`** Указатель, используемый для получения доступа к экземпляру класса в процедурах окна.

`m_dwThreadID`<br/>
Идентификатор потока текущего экземпляра класса.

`m_pNext`<br/>
Указатель на следующий `_AtlCreateWndData` объект.

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="see-also"></a>См. также раздел

[Классы и структуры](../../atl/reference/atl-classes.md)
