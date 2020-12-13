---
description: 'Дополнительные сведения о: Чеапптрлист Class'
title: Класс Чеапптрлист
ms.date: 11/04/2016
f1_keywords:
- CHeapPtrList
- ATLCOLL/ATL::CHeapPtrList
- ATLCOLL/ATL::CHeapPtrList::CHeapPtrList
helpviewer_keywords:
- CHeapPtrList class
ms.assetid: cc70e585-362a-4007-81db-c705eb181226
ms.openlocfilehash: 7e3a97280f7abcd4b7efebf6726ac062215912d2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141600"
---
# <a name="cheapptrlist-class"></a>Класс Чеапптрлист

Этот класс предоставляет методы, полезные при построении списка указателей на кучу.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<typename E, class Allocator = ATL::CCRTAllocator>
class CHeapPtrList
   : public CAtlList<ATL::CHeapPtr<E, Allocator>,
                     CHeapPtrElementTraits<E, Allocator>>
```

#### <a name="parameters"></a>Параметры

*E*<br/>
Тип объекта, который должен храниться в классе коллекции.

*Выделен*<br/>
Используемый класс выделения памяти. Значение по умолчанию — [ккрталлокатор](../../atl/reference/ccrtallocator-class.md).

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Чеапптрлист:: Чеапптрлист](#cheapptrlist)|Конструктор.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет конструктор и наследует методы от [катллист](../../atl/reference/catllist-class.md) и [чеапптрелементтраитс](../../atl/reference/cheapptrelementtraits-class.md) для облегчения создания объекта класса коллекции, в котором хранятся указатели кучи.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[катллист](../../atl/reference/catllist-class.md)

`CHeapPtrList`

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cheapptrlistcheapptrlist"></a><a name="cheapptrlist"></a> Чеапптрлист:: Чеапптрлист

Конструктор.

```
CHeapPtrList(UINT nBlockSize = 10) throw();
```

### <a name="parameters"></a>Параметры

*нблокксизе*<br/>
Размер блока.

### <a name="remarks"></a>Комментарии

Размер блока — это мера объема памяти, выделенной при необходимости нового элемента. Большие размеры блоков сокращают число вызовов подпрограмм выделения памяти, но используют больше ресурсов.

## <a name="see-also"></a>См. также раздел

[Класс Катллист](../../atl/reference/catllist-class.md)<br/>
[Класс Чеапптр](../../atl/reference/cheapptr-class.md)<br/>
[Класс Чеапптрелементтраитс](../../atl/reference/cheapptrelementtraits-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
