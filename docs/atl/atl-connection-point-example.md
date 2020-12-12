---
description: Дополнительные сведения см. в примере точки подключения ATL.
title: Пример точки подключения ATL
ms.date: 11/04/2016
helpviewer_keywords:
- connection points [C++], examples
- examples [ATL]
ms.assetid: a49721b7-f308-43de-8868-f662a94bc81a
ms.openlocfilehash: 6416720b5366838f9687f31947cac9a6824da058
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97165814"
---
# <a name="atl-connection-point-example"></a>Пример точки подключения ATL

В этом примере показан объект, который поддерживает [ипропертинотифисинк](/windows/win32/api/ocidl/nn-ocidl-ipropertynotifysink) в качестве исходящего интерфейса:

[!code-cpp[NVC_ATL_Windowing#84](../atl/codesnippet/cpp/atl-connection-point-example_1.h)]

При указании `IPropertyNotifySink` в качестве исходящего интерфейса можно использовать класс [ипропертинотифисинккп](../atl/reference/ipropertynotifysinkcp-class.md) вместо `IConnectionPointImpl` . Пример:

[!code-cpp[NVC_ATL_Windowing#85](../atl/codesnippet/cpp/atl-connection-point-example_2.h)]

## <a name="see-also"></a>См. также раздел

[Точка подключения](../atl/atl-connection-points.md)
