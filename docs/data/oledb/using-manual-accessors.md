---
description: 'Дополнительные сведения: использование методов доступа вручную'
title: Использование методов ручного доступа
ms.date: 10/24/2018
helpviewer_keywords:
- command handling, OLE DB Templates
- manual accessors
- accessors [C++], manual
ms.assetid: 29f00a89-0240-482b-8413-4120b9644672
ms.openlocfilehash: 73363be83e06a3eeced114dc90c65f82601a4a16
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332471"
---
# <a name="using-manual-accessors"></a>Использование методов ручного доступа

При обработке неизвестной команды необходимо выполнить четыре действия:

- Определение параметров

- Выполнение команды

- Определение выходных столбцов

- Проверьте, есть ли несколько возвращаемых наборов строк

Чтобы выполнить эти действия с помощью шаблонов потребителей OLE DB, используйте `CManualAccessor` класс и выполните следующие действия.

1. Откройте `CCommand` объект с помощью `CManualAccessor` в качестве параметра шаблона.

    ```cpp
    CCommand<CManualAccessor, CRowset, CMultipleResults> rs;
    ```

1. Запросите сеанс для `IDBSchemaRowset` интерфейса и используйте набор строк Parameters процедуры. Если `IDBSchemaRowset` интерфейс недоступен, запросите `ICommandWithParameters` интерфейс. Вызов `GetParameterInfo` для получения сведений. Если ни один из интерфейсов недоступен, можно предположить, что параметры отсутствуют.

1. Для каждого параметра вызовите, `AddParameterEntry` чтобы добавить параметры и задать их.

1. Откройте набор строк, но задайте для параметра привязки значение **`false`** .

1. Вызовите метод `GetColumnInfo` , чтобы получить выходные столбцы. Используйте `AddBindEntry` для добавления выходного столбца в привязку.

1. Вызовите `GetNextResult` , чтобы определить, доступны ли дополнительные наборы строк. Повторите шаги с 2 по 5.

Пример метода доступа вручную см `CDBListView::CallProcedure` . в разделе примера [дбвиевер](https://github.com/Microsoft/VCSamples/tree/master/VC2010Samples/ATL/OLEDB/Consumer) .

## <a name="see-also"></a>См. также раздел

[Использование методов доступа](../../data/oledb/using-accessors.md)
