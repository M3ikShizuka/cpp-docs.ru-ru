---
description: 'Дополнительные сведения о: Ккустомсессион (Кустомсесс. H)'
title: CCustomSession (CustomSess.H)
ms.date: 10/22/2018
f1_keywords:
- cmyprovidersession
- myprovidersess.h
- ccustomsession
- customsess.h
helpviewer_keywords:
- CMyProviderSession class in MyProviderSess.H
- OLE DB providers, wizard-generated files
- CCustomSession class in CustomSess.H
ms.assetid: d37ad471-cf05-49c5-aa47-cd10824d777f
ms.openlocfilehash: 0c090e01b5cef1bc0fccad8a1c23948fb9ea09b3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170429"
---
# <a name="ccustomsession-customsessh"></a>CCustomSession (CustomSess.H)

*Пользовательский элемент* Подряд. H содержит объявление и реализацию для объекта сеанса OLE DB. Объект источника данных создает объект сеанса и представляет диалог между потребителем и поставщиком. Для одного источника данных можно открыть несколько одновременных сеансов. Список наследования для `CCustomSession` приведен ниже.

```cpp
/////////////////////////////////////////////////////////////////////////
// CCustomSession
class ATL_NO_VTABLE CCustomSession :
   public CComObjectRootEx<CComSingleThreadModel>,
   public IGetDataSourceImpl<CCustomSession>,
   public IOpenRowsetImpl<CCustomSession>,
   public ISessionPropertiesImpl<CCustomSession>,
   public IObjectWithSiteSessionImpl<CCustomSession>,
   public IDBSchemaRowsetImpl<CCustomSession>,
   public IDBCreateCommandImpl<CCustomSession, CCustomCommand>
```

Объект сеанса наследует от `IGetDataSource` ,, `IOpenRowset` `ISessionProperties` и `IDBCreateCommand` . `IGetDataSource`Интерфейс позволяет сеансу получить источник данных, создавший его. Это полезно, если необходимо получить свойства из созданного источника данных или другие сведения, которые может предоставить источник данных. `ISessionProperties`Интерфейс обрабатывает все свойства сеанса. `IOpenRowset`Интерфейсы и `IDBCreateCommand` используются для работы с базой данных. Если поставщик поддерживает команды, он реализует `IDBCreateCommand` интерфейс. Он используется для создания объекта Command, который может выполнять команды. Поставщик всегда реализует `IOpenRowset` объект. Он используется для создания набора строк от поставщика. Это набор строк по умолчанию (например, `"select * from mytable"` ) от поставщика.

Мастер также создает три класса сеанса: `CCustomSessionColSchema` , `CCustomSessionPTSchema` и `CCustomSessionTRSchema` . Эти сеансы используются для наборов строк схемы. Наборы строк схемы позволяют поставщику возвращать метаданные потребителю, не требуя от потребителя необходимости выполнять запрос или получать данные. Получение метаданных может быть гораздо быстрее, чем поиск возможностей поставщика.

Спецификация OLE DB требует, чтобы поставщики, реализующие `IDBSchemaRowset` интерфейс, поддерживали три типа наборов строк схемы: DBSCHEMA_COLUMNS, DBSCHEMA_PROVIDER_TYPES и DBSCHEMA_TABLES. Мастер создает реализации для каждого набора строк схемы. Каждый класс, созданный мастером, содержит `Execute` метод. В этом `Execute` методе можно вернуть данные поставщику о том, какие таблицы, столбцы и типы данных поддерживаются. Эти данные известны во время компиляции.

## <a name="see-also"></a>См. также раздел

[Файлы Wizard-Generated поставщика](../../data/oledb/provider-wizard-generated-files.md)<br/>
