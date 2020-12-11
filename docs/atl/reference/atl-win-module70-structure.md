---
description: 'Дополнительные сведения: структура _ATL_WIN_MODULE70'
title: Структура _ATL_WIN_MODULE70
ms.date: 11/04/2016
f1_keywords:
- _ATL_WIN_MODULE70
- ATL::_ATL_WIN_MODULE70
- ATL._ATL_WIN_MODULE70
helpviewer_keywords:
- _ATL_WIN_MODULE70 structure
- ATL_WIN_MODULE70 structure
ms.assetid: a0aaf3ea-ca77-46ec-bd53-4dfb61dffbea
ms.openlocfilehash: 11b7fdad71fa8c7b615a0e6873571c38420c9b5d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158625"
---
# <a name="_atl_win_module70-structure"></a>Структура _ATL_WIN_MODULE70

Используется в коде окон в ATL.

## <a name="syntax"></a>Синтаксис

```cpp
struct _ATL_WIN_MODULE70 {
    UNIT cbSize;
    CRITICAL_SECTION m_csWindowCreate;
    _AtlCreateWndData* m_pCreateWndList;
    CSimpleArray<ATOM> m_rgWindowClassAtoms;
};
```

## <a name="members"></a>Члены

`cbSize`<br/>
Размер структуры, используемый для управления версиями.

`m_csWindowCreate`<br/>
Используется для сериализации доступа к коду регистрации окна. Используется внутренне библиотекой ATL.

`m_pCreateWndList`<br/>
Используется для привязки окон к своим объектам. Используется внутренне библиотекой ATL.

`m_rgWindowClassAtoms`<br/>
Используется для трассировки регистраций классов окон, чтобы их можно было правильно отменить регистрацию при завершении работы. Используется внутренне библиотекой ATL.

## <a name="remarks"></a>Комментарии

[_ATL_WIN_MODULE](atl-typedefs.md#_atl_win_module) определяется как typedef для `_ATL_WIN_MODULE70` .

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="see-also"></a>См. также раздел

[Классы и структуры](../../atl/reference/atl-classes.md)
