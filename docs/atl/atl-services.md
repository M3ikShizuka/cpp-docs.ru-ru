---
description: 'Дополнительные сведения: службы ATL'
title: Службы ATL
ms.date: 11/04/2016
helpviewer_keywords:
- CServiceModule class
- COM objects, ATL
- services, ATL
- ATL services
ms.assetid: 8c09d1a8-7548-4d2c-947c-9d795a81659b
ms.openlocfilehash: 1cb1f526434cefe57dc4675d592f836e04a6cdb6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97148607"
---
# <a name="atl-services"></a>Службы ATL

Чтобы создать COM-объект ATL, чтобы он выполнялся в службе, просто выберите Служба (EXE) в списке параметров сервера в мастере проектов ATL. Затем мастер создаст класс, производный от `CAtlServiceModuleT` , для реализации службы.

Если COM-объект ATL создан как служба, он будет зарегистрирован только как локальный сервер и не будет отображаться в списке служб на панели управления. Это объясняется тем, что проще отлаживать службу как локальный сервер, чем служба. Чтобы установить его как службу, выполните в командной строке следующую команду:

`YourEXE` `.exe /Service`

Чтобы удалить его, выполните следующую команду:

`YourEXE` `.exe /UnregServer`

В первых четырех подразделах этого раздела обсуждаются действия, происходящие во время выполнения `CAtlServiceModuleT` функций элементов. Эти разделы отображаются в той же последовательности, что и функции, которые обычно называются. Чтобы улучшить понимание этих разделов, рекомендуется использовать исходный код, созданный мастером проектов ATL, в качестве ссылки. Вот эти первые четыре раздела:

- [Функция функция CAtlServiceModuleT:: Start](../atl/reference/catlservicemodulet-class.md#start)

- [Функция функция CAtlServiceModuleT:: ServiceMain](../atl/reference/catlservicemodulet-class.md#servicemain)

- [Функция функция CAtlServiceModuleT:: Run](../atl/reference/catlservicemodulet-class.md#run)

- [Функция функция CAtlServiceModuleT:: Handler](../atl/reference/catlservicemodulet-class.md#handler)

В последних трех разделах обсуждаются основные понятия, связанные с разработкой службы.

- [Записи реестра](../atl/registry-entries.md) для служб ATL

- [DCOMCNFG](../atl/dcomcnfg.md)

- [Советы по отладке](../atl/debugging-tips.md) для служб ATL

## <a name="see-also"></a>См. также раздел

[Основные понятия](../atl/active-template-library-atl-concepts.md)
