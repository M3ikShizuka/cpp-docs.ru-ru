---
description: 'Дополнительные сведения о: Цинтерфацелист Class'
title: Класс Цинтерфацелист
ms.date: 11/04/2016
f1_keywords:
- CInterfaceList
- ATLCOLL/ATL::CInterfaceList
- ATLCOLL/ATL::CInterfaceList::CInterfaceList
helpviewer_keywords:
- CInterfaceList class
ms.assetid: 2077764d-25e5-4b3d-96c8-08a287bbcd25
ms.openlocfilehash: 2612ba4700466bb877f84978c55bfd018f1dd286
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141535"
---
# <a name="cinterfacelist-class"></a>Класс Цинтерфацелист

Этот класс предоставляет методы, полезные при создании списка указателей на COM-интерфейс.

## <a name="syntax"></a>Синтаксис

```
template<class I, const IID* piid =& __uuidof(I)>
class CInterfaceList
   : public CAtlList<ATL::CComQIPtr<I, piid>,
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
|[Цинтерфацелист:: Цинтерфацелист](#cinterfacelist)|Конструктор для списка интерфейсов.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет конструктор и производные методы для создания списка указателей на COM-интерфейс. Используйте [Цинтерфацеаррай](../../atl/reference/cinterfacearray-class.md) , если требуется массив.

Дополнительные сведения см. в разделе [классы коллекций ATL](../../atl/atl-collection-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[катллист](../../atl/reference/catllist-class.md)

`CInterfaceList`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cinterfacelistcinterfacelist"></a><a name="cinterfacelist"></a> Цинтерфацелист:: Цинтерфацелист

Конструктор для списка интерфейсов.

```
CInterfaceList(UINT nBlockSize = 10) throw();
```

### <a name="parameters"></a>Параметры

*нблокксизе*<br/>
Размер блока со значением по умолчанию 10.

### <a name="remarks"></a>Комментарии

Размер блока — это мера объема памяти, выделенной при необходимости нового элемента. Большие размеры блоков сокращают число вызовов подпрограмм выделения памяти, но используют больше ресурсов.

## <a name="see-also"></a>См. также раздел

[Класс Катллист](../../atl/reference/catllist-class.md)<br/>
[Класс CComQIPtr](../../atl/reference/ccomqiptr-class.md)<br/>
[Класс Ккомкиптрелементтраитс](../../atl/reference/ccomqiptrelementtraits-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
