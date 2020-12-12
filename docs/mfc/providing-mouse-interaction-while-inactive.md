---
description: 'Дополнительные сведения: предоставление взаимодействия с мышью во время неактивности'
title: Обеспечение взаимодействия с мышью в неактивном режиме
ms.date: 11/04/2016
helpviewer_keywords:
- MFC ActiveX controls [MFC], mouse interaction
ms.assetid: b09106bf-44c7-4b9b-a6d9-0d624f16f5b3
ms.openlocfilehash: bd3c069b052b58059de5f311e4ead795400d32fe
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97248740"
---
# <a name="providing-mouse-interaction-while-inactive"></a>Обеспечение взаимодействия с мышью в неактивном режиме

Если элемент управления не активируется немедленно, можно по-прежнему обрабатывать WM_SETCURSOR и WM_MOUSEMOVE сообщения, даже если элемент управления не имеет собственного окна. Это можно сделать, включив `COleControl` реализацию `IPointerInactive` интерфейса, который по умолчанию отключен. (Описание этого интерфейса см. в *пакете SDK для ActiveX* .) Чтобы включить его, включите флаг Поинтеринактиве в набор флагов, возвращаемых [COleControl:: жетконтролфлагс](../mfc/reference/colecontrol-class.md#getcontrolflags):

[!code-cpp[NVC_MFC_AxOpt#5](../mfc/codesnippet/cpp/providing-mouse-interaction-while-inactive_1.cpp)]
[!code-cpp[NVC_MFC_AxOpt#10](../mfc/codesnippet/cpp/providing-mouse-interaction-while-inactive_2.cpp)]
[!code-cpp[NVC_MFC_AxOpt#7](../mfc/codesnippet/cpp/providing-mouse-interaction-while-inactive_3.cpp)]

Код для включения этого флага создается автоматически, если при создании элемента управления с помощью **мастера элементов управления MFC ActiveX** на странице [параметров управления](../mfc/reference/control-settings-mfc-activex-control-wizard.md) выбран параметр **уведомления указателя мыши** .

Когда `IPointerInactive` интерфейс включен, контейнер делегирует WM_SETCURSOR и WM_MOUSEMOVE в него сообщения. `COleControl`Реализация `IPointerInactive` диспетчеризации отправляет сообщения через карту сообщений элемента управления после настройки координат мыши соответствующим образом. Вы можете обрабатывать сообщения так же, как обычные сообщения в окне, добавляя соответствующие записи в схему сообщений. В обработчиках этих сообщений не следует использовать переменную-член *m_hWnd* (или любую функцию-член, которая ее использует) без предварительной проверки того, что ее значение не равно **null**.

Также может потребоваться, чтобы неактивный элемент управления был целевым объектом операции перетаскивания OLE. Это требует активации элемента управления в момент, когда пользователь перетаскивает на него объект, чтобы окно элемента управления можно было зарегистрировать как цель перетаскивания. Чтобы активация производилась во время перетаскивания, переопределите [COleControl:: жетактиватионполици](../mfc/reference/colecontrol-class.md#getactivationpolicy)и возвратите флаг POINTERINACTIVE_ACTIVATEONDRAG:

[!code-cpp[NVC_MFC_AxOpt#11](../mfc/codesnippet/cpp/providing-mouse-interaction-while-inactive_4.cpp)]

Включение `IPointerInactive` интерфейса обычно означает, что элемент управления должен поддерживать обработку сообщений мыши все время. Чтобы получить это поведение в контейнере, который не поддерживает `IPointerInactive` интерфейс, необходимо, чтобы элемент управления всегда был активирован, когда он видим, а это означает, что элемент управления должен включать флаг OLEMISC_ACTIVATEWHENVISIBLE среди прочих флагов. Однако, чтобы этот флаг не действовал в контейнере, который поддерживает `IPointerInactive` , можно также указать флаг OLEMISC_IGNOREACTIVATEWHENVISIBLE:

[!code-cpp[NVC_MFC_AxOpt#12](../mfc/codesnippet/cpp/providing-mouse-interaction-while-inactive_5.cpp)]

## <a name="see-also"></a>См. также раздел

[Элементы ActiveX в MFC. Оптимизация](../mfc/mfc-activex-controls-optimization.md)
