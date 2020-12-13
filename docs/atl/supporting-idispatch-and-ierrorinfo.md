---
description: 'Дополнительные сведения: поддержка IDispatch и IErrorInfo'
title: Поддержка IDispatch и IErrorInfo
ms.date: 11/04/2016
helpviewer_keywords:
- ISupportErrorInfoImpl method
- IErrorInfo class suppor in ATL
- IDispatchImpl class
- IDispatch class support in ATL
ms.assetid: 7db2220f-319d-4ce9-9382-d340019f14f7
ms.openlocfilehash: 4622c8811fafc9512400345e5876dd24c466bc93
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97138454"
---
# <a name="supporting-idispatch-and-ierrorinfo"></a>Поддержка IDispatch и IErrorInfo

Класс шаблона [IDispatchImpl](../atl/reference/idispatchimpl-class.md) можно использовать для предоставления реализации по умолчанию `IDispatch Interface` части любых сдвоенных интерфейсов в объекте.

Если объект использует `IErrorInfo` интерфейс для сообщения об ошибках обратно клиенту, то объект должен поддерживать `ISupportErrorInfo Interface` интерфейс. Класс шаблона [ISupportErrorInfoImpl](../atl/reference/isupporterrorinfoimpl-class.md) предоставляет простой способ реализации этого, если у вас только один интерфейс, который создает ошибки в объекте.

## <a name="see-also"></a>См. также раздел

[Основы COM-объектов ATL](../atl/fundamentals-of-atl-com-objects.md)
