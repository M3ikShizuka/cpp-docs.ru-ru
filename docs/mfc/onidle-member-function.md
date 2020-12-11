---
description: Дополнительные сведения о функции члена OnIdle
title: Функция-член OnIdle
ms.date: 11/19/2018
f1_keywords:
- OnIdle
helpviewer_keywords:
- processing messages [MFC]
- OnIdle method [MFC]
- idle loop processing [MFC]
- CWinApp class [MFC], OnIdle method [MFC]
- message handling [MFC], OnIdle method [MFC]
ms.assetid: 51adc874-0075-4f76-be1c-79283f46c10b
ms.openlocfilehash: a094b72f78db75d9f0f93ffa840d1d90cc96294c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97112262"
---
# <a name="onidle-member-function"></a>Функция-член OnIdle

Когда сообщения Windows не обрабатываются, платформа вызывает функцию-член [CWinApp](reference/cwinapp-class.md) [OnIdle](reference/cwinapp-class.md#onidle) (описанную в справочнике по библиотеке MFC).

Переопределение `OnIdle` для выполнения фоновых задач. Версия по умолчанию обновляет состояние объектов пользовательского интерфейса, таких как кнопки на панели инструментов, и выполняет очистку временных объектов, созданных платформой в ходе выполнения операций. На следующем рисунке показано, как цикл обработки сообщений вызывается, `OnIdle` когда в очереди нет сообщений.

![Процесс цикла сообщений](../mfc/media/vc387c1.gif "Процесс цикла сообщений") <br/>
Цикл обработки сообщений

Дополнительные сведения о том, что можно сделать в цикле бездействия, см. в разделе [Обработка бездействующего цикла](idle-loop-processing.md).

## <a name="see-also"></a>См. также раздел

[CWinApp: класс Application](cwinapp-the-application-class.md)
