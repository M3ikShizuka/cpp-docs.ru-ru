---
description: 'Дополнительные сведения: реализация CComObjectRootEx'
title: Реализация CComObjectRootEx
ms.date: 11/04/2016
helpviewer_keywords:
- CComObjectRoot class, implementing
- CComObjectRootEx class
ms.assetid: 79630c44-f2df-4e9e-b730-400a0ebfbd2b
ms.openlocfilehash: 235d10a8c390311230057da5dda11e5a8f093445
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152845"
---
# <a name="implementing-ccomobjectrootex"></a>Реализация CComObjectRootEx

[CComObjectRootEx](../atl/reference/ccomobjectrootex-class.md) является обязательным; все объекты ATL должны иметь один экземпляр `CComObjectRootEx` или [CComObjectRoot](../atl/reference/ccomobjectroot-class.md) в их наследовании. `CComObjectRootEx` предоставляет механизм по умолчанию `QueryInterface`, основанный на записях сопоставления COM.

Посредством его сопоставления COM интерфейсы объекта предоставляются клиенту, когда он запрашивает интерфейс. Запрос выполняется с помощью `CComObjectRootEx::InternalQueryInterface`. `InternalQueryInterface` обрабатывает интерфейсы только в таблице сопоставлений COM.

Можно ввести интерфейсы в таблицу-сопоставлении COM с помощью макроса [COM_INTERFACE_ENTRY](reference/com-interface-entry-macros.md#com_interface_entry) или одного из его вариантов. Например, следующий код вводит интерфейсы `IDispatch`, `IBeeper` и `ISupportErrorInfo` в таблицу сопоставлений COM:

[!code-cpp[NVC_ATL_COM#1](../atl/codesnippet/cpp/implementing-ccomobjectrootex_1.h)]

## <a name="see-also"></a>См. также раздел

[Основы COM-объектов ATL](../atl/fundamentals-of-atl-com-objects.md)<br/>
[Макросы схемы COM](../atl/reference/com-map-macros.md)
