---
description: Дополнительные сведения о интерфейсах объектов наборов строк
title: Интерфейсы объекта Rowset
ms.date: 10/24/2018
helpviewer_keywords:
- interfaces, OLE DB
- OLE DB, interfaces
- rowset objects [OLE DB]
- OLE DB provider templates, object interfaces
- interfaces, list of
ms.assetid: 0d7a5d48-2fe4-434f-a84b-157c1fdc3494
ms.openlocfilehash: fc7cbb0ee7c15cc7414144334018afc93888da01
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316860"
---
# <a name="rowset-object-interfaces"></a>Интерфейсы объекта Rowset

В следующей таблице показаны обязательные и необязательные интерфейсы, определенные OLE DB для объекта набора строк.

|Интерфейс|Необходим?|Реализуется с помощью шаблонов OLE DB?|
|---------------|---------------|--------------------------------------|
|[IAccessor](/previous-versions/windows/desktop/ms719672(v=vs.85))|Обязательный|Да|
|[IColumnsInfo](/previous-versions/windows/desktop/ms724541(v=vs.85))|Обязательный|Да|
|[IConvertType](/previous-versions/windows/desktop/ms715926(v=vs.85))|Обязательный|Да|
|[IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85))|Обязательный|Да|
|[IRowsetInfo](/previous-versions/windows/desktop/ms724541(v=vs.85))|Обязательный|Да|
|[ичаптередровсет](/previous-versions/windows/desktop/ms718180(v=vs.85))|Необязательно|Нет|
|[IColumnsInfo2](/previous-versions/windows/desktop/ms712953(v=vs.85))|Необязательно|Нет|
|[IColumnsRowset](/previous-versions/windows/desktop/ms722657(v=vs.85))|Необязательно|Нет|
|[IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer)|Необязательно|Да (с помощью ATL)|
|[IDBAsynchStatus](/previous-versions/windows/desktop/ms709832(v=vs.85))|Необязательно|Нет|
|[ижетров](/previous-versions/windows/desktop/ms718047(v=vs.85))|Необязательно|Нет|
|[IRowsetChange](/previous-versions/windows/desktop/ms715790(v=vs.85))|Необязательно|Да|
|[ировсетчаптермембер](/previous-versions/windows/desktop/ms725430(v=vs.85))|Необязательно|Нет|
|[ировсеткуррентиндекс](/previous-versions/windows/desktop/ms709700(v=vs.85))|Необязательно|Нет|
|[IRowsetFind](/previous-versions/windows/desktop/ms724221(v=vs.85))|Необязательно|Нет|
|[ировсетидентити](/previous-versions/windows/desktop/ms715913(v=vs.85))|Необязательный (но требуется для поставщиков уровня 0)|Да|
|[IRowsetIndex](/previous-versions/windows/desktop/ms719604(v=vs.85))|Необязательно|Нет|
|[IRowsetLocate](/previous-versions/windows/desktop/ms721190(v=vs.85))|Необязательно|Да|
|[ировсетрефреш](/previous-versions/windows/desktop/ms714892(v=vs.85))|Необязательно|Нет|
|[IRowsetScroll](/previous-versions/windows/desktop/ms712984(v=vs.85))|Необязательно|Нет|
|[IRowsetUpdate](/previous-versions/windows/desktop/ms714401(v=vs.85))|Необязательно|Да|
|[ировсетвиев](/previous-versions/windows/desktop/ms709755(v=vs.85))|Необязательно|Нет|
|[ISupportErrorInfo](/previous-versions/windows/desktop/ms715816(v=vs.85))|Необязательно|Да|
|[ировсетбукмарк](/previous-versions/windows/desktop/ms714246(v=vs.85))|Необязательно|Нет|

Созданный мастером объект набора строк реализует `IAccessor` , `IRowset` и `IRowsetInfo` посредством наследования. `IAccessorImpl`Привязывает оба выходных столбца. `IRowset`Интерфейс обрабатывает выборку строк и данных. `IRowsetInfo`Интерфейс обрабатывает свойства набора строк.

## <a name="see-also"></a>См. также раздел

[Архитектура шаблона поставщика OLE DB](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
