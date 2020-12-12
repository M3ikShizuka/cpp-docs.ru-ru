---
description: Дополнительные сведения о том, как отправить сообщение с постоянным интервалом.
title: Практическое руководство. Отправка сообщений через определенные интервалы
ms.date: 11/04/2016
helpviewer_keywords:
- timer class, example
- sending messages at regular intervals [Concurrency Runtime]
ms.assetid: 4b60ea6c-97c8-4d69-9f7b-ad79f3548026
ms.openlocfilehash: f65226d8101ddbadaee97a16f63512b9c8dcb41e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97197288"
---
# <a name="how-to-send-a-message-at-a-regular-interval"></a>Практическое руководство. Отправка сообщений через определенные интервалы

В этом примере показано, как использовать класс Concurrency::[Timer](../../parallel/concrt/reference/timer-class.md) для отправки сообщения через обычный интервал.

## <a name="example"></a>Пример

В следующем примере объект используется `timer` для сообщения о ходе выполнения во время длительной операции. В этом примере объект связывается `timer` с объектом [Concurrency:: Call](../../parallel/concrt/reference/call-class.md) . `call`Объект выводит индикатор хода выполнения на консоль с постоянным интервалом. Метод [Concurrency:: Timer:: Start](reference/timer-class.md#start) запускает таймер в отдельном контексте. `perform_lengthy_operation`Функция вызывает функцию [Concurrency:: wait](reference/concurrency-namespace-functions.md#wait) в основном контексте для моделирования длительной операции.

[!code-cpp[concrt-report-progress#1](../../parallel/concrt/codesnippet/cpp/how-to-send-a-message-at-a-regular-interval_1.cpp)]

В этом примере выводится следующий пример выходных данных:

```Output
Performing a lengthy operation..........done.
```

## <a name="compiling-the-code"></a>Компиляция кода

Скопируйте пример кода и вставьте его в проект Visual Studio или вставьте в файл с именем, `report-progress.cpp` а затем выполните следующую команду в окне командной строки Visual Studio.

> **cl.exe/EHsc репорт-прогресс. cpp**

## <a name="see-also"></a>См. также раздел

[библиотеку асинхронных агентов](../../parallel/concrt/asynchronous-agents-library.md)<br/>
[Асинхронные блоки сообщений](../../parallel/concrt/asynchronous-message-blocks.md)<br/>
[Функции передачи сообщений](../../parallel/concrt/message-passing-functions.md)
