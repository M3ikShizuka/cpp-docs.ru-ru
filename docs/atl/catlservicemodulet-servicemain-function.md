---
description: 'Дополнительные сведения о функции: функция CAtlServiceModuleT:: ServiceMain'
title: 'Функция функция CAtlServiceModuleT:: ServiceMain'
ms.date: 11/04/2016
helpviewer_keywords:
- ServiceMain method
ms.assetid: f21408c1-1919-4dec-88d8-bf5b39ac9808
ms.openlocfilehash: 97093d13a2f13ea0d6bd4ba5db46bef45d239cc9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97148334"
---
# <a name="catlservicemoduletservicemain-function"></a>Функция функция CAtlServiceModuleT:: ServiceMain

Диспетчер управления службами вызывается `ServiceMain` при открытии приложения панели управления "службы", выборе службы и нажатии кнопки " **запустить**".

После вызова SCM `ServiceMain` служба должна предоставить SCM функцию обработчика. Эта функция позволяет SCM получать состояние службы и передавать конкретные инструкции (такие как приостановка или остановка). SCM получает эту функцию, когда служба передается в `_Handler` функцию API Win32, [регистерсервицектрлхандлер](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerw). ( `_Handler` — это статическая функция-член, которая вызывает [обработчик](../atl/reference/catlservicemodulet-class.md#handler)функции-члена, не являющейся статическим.)

При запуске служба также должна сообщать SCM о своем текущем состоянии. Это достигается путем передачи SERVICE_START_PENDING в функцию Win32 API [сбой SetServiceStatus](/windows/win32/api/winsvc/nf-winsvc-setservicestatus).

`ServiceMain` затем вызывает метод `CAtlExeModuleT::InitializeCom` , который вызывает функцию [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)интерфейса API Win32. По умолчанию `InitializeCom` передает флаг COINIT_MULTITHREADED в функцию. Этот флаг указывает, что программа является свободным потоком сервера.

Теперь `CAtlServiceModuleT::Run` вызывается для выполнения основной работы службы. `Run` будет выполняться до тех пор, пока служба не будет остановлена.

## <a name="see-also"></a>См. также раздел

[Службы](../atl/atl-services.md)<br/>
[Функция CAtlServiceModuleT:: ServiceMain](../atl/reference/catlservicemodulet-class.md#servicemain)
