---
description: Дополнительные сведения о интерфейсах объектов сеанса
title: Интерфейсы объекта Session
ms.date: 11/19/2018
helpviewer_keywords:
- session objects [OLE DB]
- session objects [OLE DB], interfaces
- OLE DB provider templates, object interfaces
- interfaces, session object
- interfaces, list of
ms.assetid: ac01a958-6dde-4bd7-8b63-94459e488335
ms.openlocfilehash: dc4f5644258b0ced4c97a5cda6de1b69abb8c2f1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286583"
---
# <a name="session-object-interfaces"></a>Интерфейсы объекта Session

В следующей таблице показаны обязательные и необязательные интерфейсы, определенные OLE DB для объекта сеанса.

|Интерфейс|Необходим?|Реализуется с помощью шаблонов OLE DB?|
|---------------|---------------|--------------------------------------|
|[IGetDataSource](/previous-versions/windows/desktop/ms709721(v=vs.85))|Обязательный|Да|
|[IOpenRowset](/previous-versions/windows/desktop/ms716946(v=vs.85))|Обязательный|Да|
|[исессионпропертиес](/previous-versions/windows/desktop/ms713721(v=vs.85))|Обязательный|Да|
|[иалтериндекс](/previous-versions/windows/desktop/ms714943(v=vs.85))|Необязательно|Нет|
|[иалтертабле](/previous-versions/windows/desktop/ms719764(v=vs.85))|Необязательно|Нет|
|[ибиндресаурце](/previous-versions/windows/desktop/ms714936(v=vs.85))|Необязательно|Нет|
|[икреатеров](/previous-versions/windows/desktop/ms716832(v=vs.85))|Необязательно|Нет|
|[IDBCreateCommand](/previous-versions/windows/desktop/ms711625(v=vs.85))|Необязательно|Да|
|[IDBSchemaRowset](/previous-versions/windows/desktop/ms713686(v=vs.85))|Необязательно|Да|
|[IIndexDefinition](/previous-versions/windows/desktop/ms711593(v=vs.85))|Необязательно|Нет|
|[ISupportErrorInfo](/previous-versions/windows/desktop/ms715816(v=vs.85))|Необязательно|Да|
|[итаблекреатион](/previous-versions/windows/desktop/ms713639(v=vs.85))|Необязательно|Нет|
|[ITableDefinition](/previous-versions/windows/desktop/ms714277(v=vs.85))|Необязательно|Нет|
|[итабледефинитионвисконстраинтс](/previous-versions/windows/desktop/ms720947(v=vs.85))|Необязательно|Нет|
|[ITransaction](/previous-versions/windows/desktop/ms723053(v=vs.85))|Необязательно|Нет|
|[ITransactionJoin](/previous-versions/windows/desktop/ms718071(v=vs.85))|Необязательно|Нет|
|[ITransactionLocal](/previous-versions/windows/desktop/ms714893(v=vs.85))|Необязательно|Нет|
|[итрансактионобжект](/previous-versions/windows/desktop/ms713659(v=vs.85))|Необязательно|Нет|

Объект Session создает объект набора строк. Если поставщик поддерживает команды, сеанс также создает объект Command ( `CCommand` , реализующий OLE DB `TCommand` ). Объект Command реализует `ICommand` интерфейс и использует `ICommand::Execute` метод для выполнения команд в наборе строк, как показано на следующем рисунке.

![Концептуальная схема поставщика](../../data/oledb/media/vc4u551.gif "Концептуальная схема поставщика")

## <a name="see-also"></a>См. также раздел

[Архитектура шаблона поставщика OLE DB](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
