---
description: 'Дополнительные сведения: структура _ATL_MODULE70'
title: Структура _ATL_MODULE70
ms.date: 11/04/2016
f1_keywords:
- _ATL_MODULE70
- ATL::_ATL_MODULE70
- ATL._ATL_MODULE70
helpviewer_keywords:
- ATL_MODULE70 structure
- _ATL_MODULE70 structure
ms.assetid: b059b2c8-dfd1-4ac9-b07d-39df638cc7b3
ms.openlocfilehash: 8a3076cebe7cab2bce49f660e8198052af393024
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97165359"
---
# <a name="_atl_module70-structure"></a>Структура _ATL_MODULE70

Содержит данные, используемые каждым модулем ATL.

## <a name="syntax"></a>Синтаксис

```cpp
struct _ATL_MODULE70 {
    UINT cbSize;
    LONG m_nLockCnt;
    _ATL_TERMFUNC_ELEM* m_pTermFuncs;
    CComCriticalSection m_csStaticDataInitAndTypeInfo;
};
```

## <a name="members"></a>Члены

`cbSize`<br/>
Размер структуры, используемый для управления версиями.

`m_nLockCnt`<br/>
Число ссылок, чтобы определить, как долго модуль должен оставаться активным.

`m_pTermFuncs`<br/>
Отслеживает функции, которые были зарегистрированы для вызова при завершении работы ATL.

`m_csStaticDataInitAndTypeInfo`<br/>
Используется для координации доступа к внутренним данным в многопоточных ситуациях.

## <a name="remarks"></a>Комментарии

[_ATL_MODULE](atl-typedefs.md#_atl_module) определяется как typedef для `_ATL_MODULE70` .

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="see-also"></a>См. также раздел

[Классы и структуры](../../atl/reference/atl-classes.md)
