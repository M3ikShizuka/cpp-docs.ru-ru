---
description: 'Дополнительные сведения о: Ипропертинотифисинккп Class'
title: Класс Ипропертинотифисинккп
ms.date: 11/04/2016
f1_keywords:
- IPropertyNotifySinkCP
- atlctl/ATL::IPropertyNotifySinkCP
helpviewer_keywords:
- connection points [C++], managing
- sinks, notifying of changes
- IPropertyNotifySinkCP class
ms.assetid: 1b41445e-bc88-4fa6-bb62-d68aacec2bd5
ms.openlocfilehash: 096a24a22634be23c7ede955c7ae49c3dd963f66
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158365"
---
# <a name="ipropertynotifysinkcp-class"></a>Класс Ипропертинотифисинккп

Этот класс предоставляет интерфейс [ипропертинотифисинк](/windows/win32/api/ocidl/nn-ocidl-ipropertynotifysink) в качестве исходящего интерфейса для подключаемого объекта.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T, class CDV = CComDynamicUnkArray>
class IPropertyNotifySinkCP
   : public IConnectionPointImpl<T, &IID_IPropertyNotifySink, CDV>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IPropertyNotifySinkCP` .

*кдв*<br/>
Класс, управляющий соединениями между точкой подключения и ее приемниками. Значение по умолчанию — [ккомдинамикункаррай](../../atl/reference/ccomdynamicunkarray-class.md), что позволяет устанавливать неограниченное число подключений. Можно также использовать [ккомункаррай](../../atl/reference/ccomunkarray-class.md), который указывает фиксированное число соединений.

## <a name="remarks"></a>Комментарии

`IPropertyNotifySinkCP` наследует все методы через его базовый класс [иконнектионпоинтимпл](../../atl/reference/iconnectionpointimpl-class.md).

Интерфейс [ипропертинотифисинк](/windows/win32/api/ocidl/nn-ocidl-ipropertynotifysink) позволяет объекту-приемнику получать уведомления об изменениях свойств. Класс `IPropertyNotifySinkCP` предоставляет этот интерфейс в качестве исходящего интерфейса для подключаемого объекта. Клиент должен реализовать `IPropertyNotifySink` методы в приемнике.

Создайте класс, производный от класса `IPropertyNotifySinkCP` , если нужно создать точку подключения, представляющую `IPropertyNotifySink` интерфейс.

Дополнительные сведения об использовании точек подключения в ATL см. в статье [точки подключения](../../atl/atl-connection-points.md).

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="see-also"></a>См. также раздел

[Класс Иконнектионпоинтимпл](../../atl/reference/iconnectionpointimpl-class.md)<br/>
[Класс Иконнектионпоинтконтаинеримпл](../../atl/reference/iconnectionpointcontainerimpl-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
