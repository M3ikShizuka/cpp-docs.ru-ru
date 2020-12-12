---
description: Дополнительные сведения см. в статье об обработке событий ATL.
title: Сводка по обработке событий ATL
ms.date: 11/04/2016
helpviewer_keywords:
- event handling, implementing
ms.assetid: e8b47ef0-0bdc-47ff-9dd6-34df11dde9a2
ms.openlocfilehash: c041de6cbd0e0852d5ce0e51d892c21c7d9a23d3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97148659"
---
# <a name="atl-event-handling-summary"></a>Сводка по обработке событий ATL

Как правило, обработка событий COM — это относительно простой процесс. Существует три основных шага:

- Реализуйте интерфейс событий для объекта.

- Посоветуйте источнику событий, что объект хочет получать события.

- Если объекту больше не требуется получение событий, следует снять с него порекомендовать источник события.

## <a name="implementing-the-interface"></a>Реализация интерфейса

Существует четыре основных способа реализации интерфейса с помощью ATL.

|Наследование от |Подходит для типа интерфейса|Требует реализации всех методов *|Требуется библиотека типов во время выполнения|
|-----------------|---------------------------------|---------------------------------------------|-----------------------------------------|
|Интерфейс|Vtable|Да|Нет|
|[IDispatchImpl](../atl/reference/idispatchimpl-class.md)|Двойной режим|Да|Да|
|[IDispEventImpl](../atl/reference/idispeventimpl-class.md)|Disp-интерфейс|Нет|Да|
|[IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md)|Disp-интерфейс|Нет|Нет|

\* При использовании классов поддержки ATL не требуется реализовывать `IUnknown` `IDispatch` методы или вручную.

## <a name="advising-and-unadvising-the-event-source"></a>Рекомендуется и не рекомендуется источник событий

Существует три основных способа, которые подают и не рекомендуется использовать источник событий с помощью ATL.

|Advise, функция|Функция unadvise|Наиболее подходящим для использования с|Требуется отслеживание файла cookie|Комментарии|
|---------------------|-----------------------|--------------------------------|---------------------------------------------|--------------|
|[Атладвисе](reference/connection-point-global-functions.md#atladvise), [Ккомптрбасе:: Advise](../atl/reference/ccomptrbase-class.md#advise)|[AtlUnadvise](reference/connection-point-global-functions.md#atlunadvise)|Vtable или сдвоенные интерфейсы|Да|`AtlAdvise` является глобальной функцией ATL. `CComPtrBase::Advise` используется [CComPtr](../atl/reference/ccomptr-class.md) и [CComQIPtr](../atl/reference/ccomqiptr-class.md).|
|[IDispEventSimpleImpl::D Испевентадвисе](../atl/reference/idispeventsimpleimpl-class.md#dispeventadvise)|[IDispEventSimpleImpl::D Испевентунадвисе](../atl/reference/idispeventsimpleimpl-class.md#dispeventunadvise)|[IDispEventImpl](../atl/reference/idispeventimpl-class.md) или [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md)|Нет|Меньше параметров `AtlAdvise` , чем, так как базовый класс выполняет больше работы.|
|[Ккомкомпоситеконтрол:: Адвисесинкмап (TRUE)](../atl/reference/ccomcompositecontrol-class.md#advisesinkmap)|[Ккомкомпоситеконтрол:: Адвисесинкмап (FALSE)](../atl/reference/ccomcompositecontrol-class.md#advisesinkmap)|Элементы управления ActiveX в составных элементах управления|Нет|`CComCompositeControl::AdviseSinkMap` сообщает обо всех записях в схеме приемника событий. Одна и та же функция не рекомендует записи. Этот метод вызывается автоматически `CComCompositeControl` классом.|
|[Каксдиалогимпл:: Адвисесинкмап (TRUE)](../atl/reference/caxdialogimpl-class.md#advisesinkmap)|[Каксдиалогимпл:: Адвисесинкмап (FALSE)](../atl/reference/caxdialogimpl-class.md#advisesinkmap)|Элементы управления ActiveX в диалоговом окне|Нет|`CAxDialogImpl::AdviseSinkMap` рекомендует и не рекомендует все элементы управления ActiveX в ресурсе диалога. Это делается автоматически.|

## <a name="see-also"></a>См. также раздел

[Обработка событий](../atl/event-handling-and-atl.md)<br/>
[Поддержка IDispEventImpl](../atl/supporting-idispeventimpl.md)
