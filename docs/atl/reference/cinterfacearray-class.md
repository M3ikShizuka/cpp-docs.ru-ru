---
description: 'Дополнительные сведения о: Цинтерфацеаррай Class'
title: Класс Цинтерфацеаррай
ms.date: 11/04/2016
f1_keywords:
- CInterfaceArray
- ATLCOLL/ATL::CInterfaceArray
- ATLCOLL/ATL::CInterfaceArray::CInterfaceArray
helpviewer_keywords:
- CInterfaceArray class
ms.assetid: 1f29cf66-a086-4a7b-b6a8-64f73da39f79
ms.openlocfilehash: 6dbe382682b8411d7562d1d0ff75f0ef587396f2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141548"
---
# <a name="cinterfacearray-class"></a>Класс Цинтерфацеаррай

Этот класс предоставляет методы, полезные при построении массива указателей на COM-интерфейс.

## <a name="syntax"></a>Синтаксис

```
template <class I, const IID* piid=& __uuidof(I)>
class CInterfaceArray :
   public CAtlArray<ATL::CComQIPtr<I, piid>,
                    CComQIPtrElementTraits<I, piid>>
```

#### <a name="parameters"></a>Параметры

*I*<br/>
COM-интерфейс, указывающий тип сохраняемого указателя.

*пиид*<br/>
Указатель на идентификатор IID *I*.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Цинтерфацеаррай:: Цинтерфацеаррай](#cinterfacearray)|Конструктор для массива интерфейсов.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет конструктор и производные методы для создания массива указателей на COM-интерфейс. Используйте [Цинтерфацелист](../../atl/reference/cinterfacelist-class.md) , если требуется список.

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CAtlArray`

`CInterfaceArray`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cinterfacearraycinterfacearray"></a><a name="cinterfacearray"></a> Цинтерфацеаррай:: Цинтерфацеаррай

Конструктор.

```
CInterfaceArray() throw();
```

### <a name="remarks"></a>Комментарии

Инициализирует массив интеллектуальных указателей.

## <a name="see-also"></a>См. также раздел

[Класс CAtlArray](../../atl/reference/catlarray-class.md)<br/>
[Класс CComQIPtr](../../atl/reference/ccomqiptr-class.md)<br/>
[Класс Ккомкиптрелементтраитс](../../atl/reference/ccomqiptrelementtraits-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
