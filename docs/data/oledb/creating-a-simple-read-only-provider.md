---
description: 'Дополнительные сведения: создание простого поставщика Read-Only'
title: Создание простого поставщика только для чтения
ms.date: 05/09/2019
helpviewer_keywords:
- OLE DB providers, creating
- OLE DB provider templates, creating providers
ms.assetid: ade8ccdd-9ea4-4e46-a964-18460c2a2401
ms.openlocfilehash: 1904e850bc6a681e13e4799a2822963932ad9dfc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323224"
---
# <a name="creating-a-simple-read-only-provider"></a>Создание простого поставщика только для чтения

::: moniker range="msvc-160"

Мастер поставщика OLE DB в ATL недоступен в Visual Studio 2019 и более поздних версиях.

::: moniker-end

::: moniker range="<=msvc-150"

После создания поставщика OLE DB с помощью **мастера проектов ATL** и **мастера поставщика OLE DB в ATL** вы можете добавить другие функциональные возможности, поддержку которых нужно обеспечить. Начните разработку вашего поставщика с изучения того, какие данные вы будете отправлять объекту-получателю и при каких условиях. Особенно важно определить, требуется ли поддержка команд, транзакций и других дополнительных объектов. Качественное планирование процесса ускорит реализацию и тестирование.

Пример разбит на две части:

- В первой части показано, как [создать простого поставщика с доступом только для чтения](../../data/oledb/implementing-the-simple-read-only-provider.md), который считывает пару строк.

- Во второй части показано, как [улучшить простого поставщика с доступом только для чтения](../../data/oledb/enhancing-the-simple-read-only-provider.md), добавив интерфейс `IRowsetLocate`.

::: moniker-end

## <a name="see-also"></a>См. также раздел

[Создание поставщика OLE DB](../../data/oledb/creating-an-ole-db-provider.md)<br/>
