---
description: 'Дополнительные сведения о: Ккустомкомманд (Кустомрс. H)'
title: CCustomCommand (CustomRS.H)
ms.date: 10/22/2018
f1_keywords:
- cmyprovidercommand
- ccustomcommand
helpviewer_keywords:
- OLE DB providers, wizard-generated files
- CMyProviderCommand class in MyProviderRS.H
- CCustomCommand class in CustomRS.H
ms.assetid: b30b956e-cc91-4cf5-9fe6-f8b1ce9cc2a5
ms.openlocfilehash: 35b0e1a1628920a85343a52ce4a003302468884b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170507"
---
# <a name="ccustomcommand-customrsh"></a>CCustomCommand (CustomRS.H)

`CCustomCommand`Класс является реализацией для объекта команды поставщика. Он предоставляет реализацию для `IAccessor` `ICommandText` `ICommandProperties` интерфейсов, и. `IAccessor`Интерфейс такой же, что и в наборе строк. Объект Command использует метод доступа для указания привязок для параметров. Объект набора строк использует их для указания привязок для выходных столбцов. `ICommandText`Интерфейс — это удобный способ указания команды в текстовом виде. В этом примере `ICommandText` интерфейс используется позже при добавлении пользовательского кода. Он также переопределяет `ICommand::Execute` метод. `ICommandProperties`Интерфейс обрабатывает все свойства для объектов Command и Rowset.

```cpp
// CCustomCommand
class ATL_NO_VTABLE CCustomCommand :
class ATL_NO_VTABLE CCustomCommand :
   public CComObjectRootEx<CComSingleThreadModel>,
   public IAccessorImpl<CCustomCommand>,
   public ICommandTextImpl<CCustomCommand>,
   public ICommandPropertiesImpl<CCustomCommand>,
   public IObjectWithSiteImpl<CCustomCommand>,
   public IConvertTypeImpl<CCustomCommand>,
   public IColumnsInfoImpl<CCustomCommand>
```

`IAccessor`Интерфейс управляет всеми привязками, используемыми в командах и наборах строк. Потребитель вызывает `IAccessor::CreateAccessor` массив `DBBINDING` структур. Каждая `DBBINDING` структура содержит сведения о том, как должны обрабатываться привязки столбцов (например, тип и длина). Поставщик получает структуры, а затем определяет способ передачи данных и необходимость каких бы то ни было преобразований. `IAccessor`Интерфейс используется в объекте Command для управления параметрами в команде.

Объект Command также предоставляет реализацию `IColumnsInfo` . Для OLE DB требуется `IColumnsInfo` интерфейс. Интерфейс позволяет потребителю получать сведения о параметрах из команды. Объект набора строк использует `IColumnsInfo` интерфейс для возвращения сведений о выходных столбцах поставщику.

Поставщик также содержит интерфейс с именем `IObjectWithSite` . `IObjectWithSite`Интерфейс был реализован в ATL 2,0 и позволяет разработчику передавать сведения о себе своему дочернему элементу. Объект Command использует эти `IObjectWithSite` сведения, чтобы сообщить всем созданным объектам набора строк о том, кто их создал.

## <a name="see-also"></a>См. также раздел

[Файлы Wizard-Generated поставщика](../../data/oledb/provider-wizard-generated-files.md)
