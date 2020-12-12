---
description: 'Дополнительные сведения: сопоставления свойств'
title: Сопоставления свойств
ms.date: 10/24/2018
helpviewer_keywords:
- OLE DB providers, properties
- maps, property
- property maps
ms.assetid: 44abde56-90ad-4612-854e-d2fa5426fa80
ms.openlocfilehash: 30b277451d871de45902661f7b7e56cbc7409c97
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316912"
---
# <a name="property-maps"></a>Сопоставления свойств

С помощью сеанса, набора строк и необязательного объекта команды каждый поставщик поддерживает одно или несколько свойств. Эти свойства определяются в сопоставлениях свойств, которые хранятся в файлах заголовков, созданных **мастером OLE DB Provider**. Каждый файл заголовка содержит карту для свойств в группе свойств OLE DB, определенной для объекта или объектов, определенных в этом файле. Файл заголовка, содержащий объект источника данных, также содержит карту свойства для [свойств DataSource](/previous-versions/windows/desktop/ms724188(v=vs.85)). `Session.h` содержит карту свойств для [свойств сеанса](/previous-versions/windows/desktop/ms714221(v=vs.85)). Набор строк и командные объекты находятся в одном файле заголовка с именем *ProjectName* RS. h. Эти свойства являются элементами группы [свойств набора строк](/previous-versions/windows/desktop/ms711252(v=vs.85)) .

## <a name="see-also"></a>См. также раздел

[Архитектура шаблона поставщика OLE DB](../../data/oledb/ole-db-provider-template-architecture.md)<br/>
