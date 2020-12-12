---
description: 'Дополнительные сведения: файлы Wizard-Generated поставщика'
title: Созданные мастером поставщика файлы
ms.date: 05/09/2019
helpviewer_keywords:
- OLE DB providers, wizard-generated files
ms.assetid: 6e1ac94b-eb90-4abf-82b3-06944b947ebc
ms.openlocfilehash: 95c9641f10acef4a55b8de15752eb125e75d874a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316899"
---
# <a name="provider-wizard-generated-files"></a>Созданные мастером поставщика файлы

::: moniker range="msvc-160"

Мастер поставщика OLE DB в ATL недоступен в Visual Studio 2019 и более поздних версиях.

::: moniker-end

::: moniker range="<=msvc-150"

**Мастер поставщика OLE DB в ATL** создает следующие файлы. В указанных ниже разделах используется короткое имя *Custom*, но точные имена файлов зависят от выбора при создании поставщика.

|Имя файла|Описание|
|---------------|-----------------|
|*Custom* RS.cpp|Содержит вспомогательный метод `Execute` команды и схему столбцов поставщика.|
|*Custom* DS.h|Реализует объект источника данных. Этот файл заголовка содержит схему свойств для свойств источника данных.|
|*Custom* RS.h|Реализует объекты команды и набора строк. Этот файл заголовка содержит схему свойств для набора строк и свойств команды.|
|*Custom* Sess.h|Реализует объект сеанса. Этот файл заголовка содержит схему свойств для свойств сеанса.|
|*Custom*.rgs|Содержит зарегистрированные объекты, создаваемые **мастером поставщика OLE DB**.|

::: moniker-end

## <a name="see-also"></a>См. также раздел

[Создание поставщика OLE DB](../../data/oledb/creating-an-ole-db-provider.md)<br/>
