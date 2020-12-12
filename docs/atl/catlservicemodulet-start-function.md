---
description: 'См. Дополнительные сведения о функции функция CAtlServiceModuleT:: Start.'
title: 'Функция функция CAtlServiceModuleT:: Start'
ms.date: 11/04/2016
helpviewer_keywords:
- Start method
ms.assetid: b5193a23-41bc-42d2-8d55-3eb43dc62238
ms.openlocfilehash: cfdae47f88c7957a4470da3129f3d3e071614276
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97148321"
---
# <a name="catlservicemoduletstart-function"></a>Функция функция CAtlServiceModuleT:: Start

При запуске службы `_tWinMain` вызывает метод `CAtlServiceModuleT::WinMain` , который, в свою очередь, вызывает `CAtlServiceModuleT::Start` .

`CAtlServiceModuleT::Start` настраивает массив `SERVICE_TABLE_ENTRY` структур, которые сопоставляют каждую службу с ее функцией запуска. Затем этот массив передается в функцию API Win32 [сбой StartServiceCtrlDispatcher](/windows/win32/api/winsvc/nf-winsvc-startservicectrldispatcherw). Теоретически один исполняемый файл может работать с несколькими службами, и массив может иметь несколько `SERVICE_TABLE_ENTRY` структур. Однако в настоящее время служба, созданная библиотекой ATL, поддерживает только одну службу на каждый исполняемый файл. Таким образом, массив содержит одну запись, которая содержит имя службы и `_ServiceMain` функцию Startup. `_ServiceMain` — Это статическая функция-член `CAtlServiceModuleT` , которая вызывает нестатичную функцию-член, `ServiceMain` .

> [!NOTE]
> Сбой `StartServiceCtrlDispatcher` подключения к диспетчеру управления службами (SCM), вероятно, означает, что программа не запущена как служба. В этом случае программа вызывает `CAtlServiceModuleT::Run` напрямую, чтобы программа могла работать как локальный сервер. Дополнительные сведения о запуске программы в качестве локального сервера см. в разделе [Советы по отладке](../atl/debugging-tips.md).

## <a name="see-also"></a>См. также раздел

[Службы](../atl/atl-services.md)<br/>
[Функция CAtlServiceModuleT:: Start](../atl/reference/catlservicemodulet-class.md#start)
