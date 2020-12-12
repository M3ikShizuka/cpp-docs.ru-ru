---
description: Дополнительные сведения см. в статье как использовать отмену для прерывания работы параллельного цикла.
title: Практическое руководство. Использование отмены для выхода из параллельного цикла
ms.date: 11/04/2016
helpviewer_keywords:
- writing a parallel search algorithm [Concurrency Runtime]
- parallel search algorithm, writing [Concurrency Runtime]
ms.assetid: 421cd2de-f058-465f-b890-dd8fcc0df273
ms.openlocfilehash: 0d2817e3a2645cb01d652b7858176ffce6df73c4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97172522"
---
# <a name="how-to-use-cancellation-to-break-from-a-parallel-loop"></a>Практическое руководство. Использование отмены для выхода из параллельного цикла

В этом примере показано, как использовать отмену для реализации простого алгоритма параллельного поиска.

## <a name="example"></a>Пример

В следующем примере отмена используется для поиска элемента в массиве. `parallel_find_any`Функция использует алгоритм [arallel_for concurrency::p](reference/concurrency-namespace-functions.md#parallel_for) и функцию [Concurrency:: run_with_cancellation_token](reference/concurrency-namespace-functions.md#run_with_cancellation_token) для поиска расположения, которое содержит заданное значение. Когда параллельный цикл находит значение, он вызывает метод [Concurrency:: cancellation_token_source:: Cancel](reference/cancellation-token-source-class.md#cancel) для отмены будущей работы.

[!code-cpp[concrt-parallel-array-search#1](../../parallel/concrt/codesnippet/cpp/how-to-use-cancellation-to-break-from-a-parallel-loop_1.cpp)]

Алгоритм [arallel_for Concurrency::p](reference/concurrency-namespace-functions.md#parallel_for) действует параллельно. Таким образом, он не выполняет операции в предварительно определенном порядке. Если массив содержит несколько экземпляров значения, результат может быть любой из его позиций.

## <a name="compiling-the-code"></a>Компиляция кода

Скопируйте пример кода и вставьте его в проект Visual Studio или вставьте в файл с именем, `parallel-array-search.cpp` а затем выполните следующую команду в окне командной строки Visual Studio.

> **cl.exe/EHsc Параллел-аррай-СЕАРЧ. cpp**

## <a name="see-also"></a>См. также раздел

[Отмена в библиотеке параллельных шаблонов](cancellation-in-the-ppl.md)<br/>
[Параллельные алгоритмы](../../parallel/concrt/parallel-algorithms.md)<br/>
[Функция parallel_for](reference/concurrency-namespace-functions.md#parallel_for)<br/>
[Класс cancellation_token_source](../../parallel/concrt/reference/cancellation-token-source-class.md)
