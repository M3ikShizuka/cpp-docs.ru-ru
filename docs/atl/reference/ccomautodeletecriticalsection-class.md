---
description: 'Дополнительные сведения о: Ккомаутоделетекритикалсектион Class'
title: Класс Ккомаутоделетекритикалсектион
ms.date: 11/04/2016
f1_keywords:
- CComAutoDeleteCriticalSection
- atlcore/ATL::CComAutoDeleteCriticalSection
helpviewer_keywords:
- CComAutoDeleteCriticalSection class
ms.assetid: 2396dbea-1c60-4841-b50e-c4e18af311a3
ms.openlocfilehash: 3c65108917b28b9e4e17210afc54eab6814302b7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152338"
---
# <a name="ccomautodeletecriticalsection-class"></a>Класс Ккомаутоделетекритикалсектион

Этот класс предоставляет методы для получения и освобождения владения объектом критической секции.

## <a name="syntax"></a>Синтаксис

```
class CComAutoDeleteCriticalSection : public CComSafeDeleteCriticalSection
```

## <a name="remarks"></a>Remarks

`CComAutoDeleteCriticalSection` является производным от класса [ккомсафеделетекритикалсектион](../../atl/reference/ccomsafedeletecriticalsection-class.md). Однако `CComAutoDeleteCriticalSection` переопределяет метод [Term](ccomsafedeletecriticalsection-class.md#term) на **`private`** доступ, что приводит к принудительной очистке внутренней памяти только в том случае, если экземпляры этого класса выходят за пределы области или явно удаляются из памяти.

Этот класс не предоставляет дополнительных методов по отношению к базовому классу. Дополнительные сведения о вспомогательных классах критической секции см. в разделе [ккомсафеделетекритикалсектион](../../atl/reference/ccomsafedeletecriticalsection-class.md) и [ккомкритикалсектион](../../atl/reference/ccomcriticalsection-class.md) .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[ккомкритикалсектион](../../atl/reference/ccomcriticalsection-class.md)

[ккомсафеделетекритикалсектион](../../atl/reference/ccomsafedeletecriticalsection-class.md)

`CComAutoDeleteCriticalSection`

## <a name="requirements"></a>Требования

**Заголовок:** атлкоре. h

## <a name="see-also"></a>См. также раздел

[Класс Ккомсафеделетекритикалсектион](../../atl/reference/ccomsafedeletecriticalsection-class.md)<br/>
[Класс Ккомкритикалсектион](../../atl/reference/ccomcriticalsection-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
