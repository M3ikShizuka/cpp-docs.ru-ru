---
description: 'Дополнительные сведения: среда выполнения с параллелизмом пошаговые руководства'
title: Пошаговые руководства по среде выполнения с параллелизмом
ms.date: 11/04/2016
helpviewer_keywords:
- walkthroughs [Concurrency Runtime]
- Concurrency Runtime, walkthroughs
ms.assetid: 7374c5e9-54eb-44bf-9ed9-5e190cfd290b
ms.openlocfilehash: 733a4dddbd800042257a89f88d93a5a6ac11de63
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257242"
---
# <a name="concurrency-runtime-walkthroughs"></a>Пошаговые руководства по среде выполнения с параллелизмом

В подразделах на основе сценариев в этом разделе показано, как использовать многие функции среда выполнения с параллелизмом.

## <a name="in-this-section"></a>в этом разделе

[Пошаговое руководство. подключение с помощью задач и HTTP-запросов XML](../../parallel/concrt/walkthrough-connecting-using-tasks-and-xml-http-requests.md)<br/>
Показывает, как использовать интерфейсы [IXMLHTTPRequest2](/windows/win32/api/msxml6/nn-msxml6-ixmlhttprequest2) и [IXMLHTTPRequest2Callback](/windows/win32/api/msxml6/nn-msxml6-ixmlhttprequest2callback) вместе с задачами для отправки запросов HTTP GET и POST к веб-службе в приложении универсальная платформа Windows (UWP).

[Пошаговое руководство. Создание приложения Agent-Based](../../parallel/concrt/walkthrough-creating-an-agent-based-application.md)<br/>
Описывает создание базового приложения на основе агента.

[Пошаговое руководство. Создание агента потока данных](../../parallel/concrt/walkthrough-creating-a-dataflow-agent.md)<br/>
Демонстрирует создание основанных на агентах приложений на основе потока данных, а не потока управления.

[Пошаговое руководство. Создание Image-Processing сети](../../parallel/concrt/walkthrough-creating-an-image-processing-network.md)<br/>
Демонстрирует создание сети асинхронных блоков сообщений, выполняющих обработку изображений.

[Пошаговое руководство. Реализация фьючерсов](../../parallel/concrt/walkthrough-implementing-futures.md)<br/>
Показывает, как асинхронно вычислять значения для последующего использования.

[Пошаговое руководство. использование Join для предотвращения взаимоблокировок](../../parallel/concrt/walkthrough-using-join-to-prevent-deadlock.md)<br/>
Использует проблему обедающих философов, чтобы продемонстрировать, как использовать класс [Concurrency:: Join](../../parallel/concrt/reference/join-class.md) для предотвращения взаимоблокировок в приложении.

[Пошаговое руководство. Удаление работы из потока User-Interface](../../parallel/concrt/walkthrough-removing-work-from-a-user-interface-thread.md)<br/>
Демонстрирует, как повысить производительность приложения MFC, которое рисует фрактал Мандельброта.

[Пошаговое руководство. Использование среда выполнения с параллелизмом в приложении COM-Enabled](../../parallel/concrt/walkthrough-using-the-concurrency-runtime-in-a-com-enabled-application.md)<br/>
Демонстрирует использование среда выполнения с параллелизмом в приложении, использующем модель COM.

[Пошаговое руководство. адаптация существующего кода к использованию упрощенных задач](../../parallel/concrt/walkthrough-adapting-existing-code-to-use-lightweight-tasks.md)<br/>
Показано, как адаптировать существующий код, использующий API Windows, для создания и выполнения потока для использования упрощенной задачи.

[Пошаговое руководство. Создание пользовательского блока сообщений](../../parallel/concrt/walkthrough-creating-a-custom-message-block.md)<br/>
Описывает создание пользовательского типа блока сообщений, который упорядочивает входящие сообщения по приоритету.

## <a name="related-sections"></a>Связанные разделы

[Среда выполнения с параллелизмом](../../parallel/concrt/concurrency-runtime.md)<br/>
Введение в платформу параллельного программирования для Visual C++.
