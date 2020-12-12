---
description: 'Дополнительные сведения о функции: функция CAtlServiceModuleT:: Handler'
title: 'Функция функция CAtlServiceModuleT:: Handler'
ms.date: 11/04/2016
helpviewer_keywords:
- Handler method
ms.assetid: 14db5f2a-be87-4774-a296-445cb6fc7b2e
ms.openlocfilehash: 934c612b6fdfd47bb9966536cc335da58fbd38c1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97148373"
---
# <a name="catlservicemodulethandler-function"></a>Функция функция CAtlServiceModuleT:: Handler

`CAtlServiceModuleT::Handler` — Это подпрограммы, которые вызываются диспетчером управления службами (SCM) для получения состояния службы и предоставления ей различных инструкций (таких как остановка или приостановка). SCM передает код операции, `Handler` чтобы указать, что должна делать служба. Служба, создаваемая библиотекой ATL по умолчанию, обрабатывает только инструкцию по ошибке. Если SCM передает инструкцию по остановке, служба сообщает SCM о том, что программа собирается остановиться. Затем служба вызывает метод `PostThreadMessage` , чтобы отправить сообщение о выходе на себя. Это завершает цикл обработки сообщений, и служба в конечном итоге будет закрыта.

Чтобы обрабатывались дополнительные инструкции, необходимо изменить `m_status` элемент данных, инициализированный в `CAtlServiceModuleT` конструкторе. Этот элемент данных сообщает SCM, какие кнопки должны быть включены при выборе службы в приложении панели управления "службы".

## <a name="see-also"></a>См. также раздел

[Службы](../atl/atl-services.md)<br/>
[Функция CAtlServiceModuleT:: Handler](../atl/reference/catlservicemodulet-class.md#handler)
