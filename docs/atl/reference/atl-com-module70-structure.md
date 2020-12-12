---
description: 'Дополнительные сведения: структура _ATL_COM_MODULE70'
title: Структура _ATL_COM_MODULE70
ms.date: 11/04/2016
f1_keywords:
- ATL::_ATL_COM_MODULE70
- ATL._ATL_COM_MODULE70
- _ATL_COM_MODULE70
helpviewer_keywords:
- _ATL_COM_MODULE70 structure
- ATL_COM_MODULE70 structure
ms.assetid: 5b0b2fd0-bdeb-4c7e-8870-78fa69ace6e6
ms.openlocfilehash: db2139d1c816c13e6da104f6a6d785ef35a07721
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97165412"
---
# <a name="_atl_com_module70-structure"></a>Структура _ATL_COM_MODULE70

Используется кодом, связанным с COM, в ATL.

## <a name="syntax"></a>Синтаксис

```cpp
struct _ATL_COM_MODULE70 {
    UINT cbSize;
    HINSTANCE m_hInstTypeLib;
    _ATL_OBJMAP_ENTRY** m_ppAutoObjMapFirst;
    _ATL_OBJMAP_ENTRY** m_ppAutoObjMapLast;
    CRITICAL_SECTION m_csObjMap;
};
```

## <a name="members"></a>Члены

`cbSize`<br/>
Размер структуры, используемый для управления версиями.

`m_hInstTypeLib`<br/>
Экземпляр Handle для библиотеки типов для этого модуля.

`m_ppAutoObjMapFirst`<br/>
Адрес элемента массива, указывающий начало записей схемы объекта для этого модуля.

`m_ppAutoObjMapLast`<br/>
Адрес элемента массива, указывающий конец записей схемы объекта для этого модуля.

`m_csObjMap`<br/>
Критическая секция для сериализации доступа к записям схемы объекта. Используется внутренне библиотекой ATL.

## <a name="remarks"></a>Комментарии

[_ATL_COM_MODULE](atl-typedefs.md#_atl_com_module) определяется как typedef _ATL_COM_MODULE70.

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="see-also"></a>См. также раздел

[Классы и структуры](../../atl/reference/atl-classes.md)
