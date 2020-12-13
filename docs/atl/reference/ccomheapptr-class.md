---
description: 'Дополнительные сведения о: Ккомхеапптр Class'
title: Класс Ккомхеапптр
ms.date: 11/04/2016
f1_keywords:
- CComHeapPtr
- ATLBASE/ATL::CComHeapPtr
- ATLBASE/ATL::CComHeapPtr::CComHeapPtr
helpviewer_keywords:
- CComHeapPtr class
ms.assetid: bd08b53d-da2b-43ab-a79c-e7c8dbbc5994
ms.openlocfilehash: 18865923e86a2392260ab1e6dedde2f37b9b4ea3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146631"
---
# <a name="ccomheapptr-class"></a>Класс Ккомхеапптр

Класс интеллектуального указателя для управления указателями кучи.

## <a name="syntax"></a>Синтаксис

```
template<typename T>
class CComHeapPtr : public CHeapPtr<T, CComAllocator>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип объекта, сохраняемый в куче.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккомхеапптр:: Ккомхеапптр](#ccomheapptr)|Конструктор.|

## <a name="remarks"></a>Комментарии

`CComHeapPtr` является производным от `CHeapPtr` , но использует [ккомаллокатор](../../atl/reference/ccomallocator-class.md) для выделения памяти с помощью подпрограмм com. Доступные методы см. в разделе [чеапптр](../../atl/reference/cheapptr-class.md) и [чеапптрбасе](../../atl/reference/cheapptrbase-class.md) .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[чеапптрбасе](../../atl/reference/cheapptrbase-class.md)

[чеапптр](../../atl/reference/cheapptr-class.md)

`CComHeapPtr`

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="ccomheapptrccomheapptr"></a><a name="ccomheapptr"></a> Ккомхеапптр:: Ккомхеапптр

Конструктор.

```
CComHeapPtr() throw();
explicit CComHeapPtr(T* pData) throw();
```

### <a name="parameters"></a>Параметры

*pData*<br/>
Существующий объект `CComHeapPtr`.

### <a name="remarks"></a>Комментарии

При необходимости можно создать указатель кучи с помощью существующего `CComHeapPtr` объекта. В этом случае новый `CComHeapPtr` объект несет ответственность за управление новым указателем и ресурсами.

## <a name="see-also"></a>См. также раздел

[Класс Чеапптр](../../atl/reference/cheapptr-class.md)<br/>
[Класс Чеапптрбасе](../../atl/reference/cheapptrbase-class.md)<br/>
[Класс Ккомаллокатор](../../atl/reference/ccomallocator-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
