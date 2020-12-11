---
description: Дополнительные сведения см. в статье как написать цикл parallel_for_each
title: Практическое руководство. Написание цикла parallel_for_each
ms.date: 11/04/2016
helpviewer_keywords:
- writing a parallel_for_each loop [Concurrency Runtime]
- parallel_for_each function, example
ms.assetid: fa9c0ba6-ace0-4f88-8681-c7c1f52aff20
ms.openlocfilehash: cb80173d3d4c78fe4d46f017d60af2c3c6659096
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97112236"
---
# <a name="how-to-write-a-parallel_for_each-loop"></a>Практическое руководство. Написание цикла parallel_for_each

В этом примере показано, как использовать алгоритм [параллелизма::p arallel_for_each](reference/concurrency-namespace-functions.md#parallel_for_each) , чтобы вычислить число простых чисел в объекте [std:: Array](../../standard-library/array-class-stl.md) параллельно.

## <a name="example"></a>Пример

В следующем примере число простых чисел в массиве вычисляются дважды. В примере сначала используется алгоритм [std:: for_each](../../standard-library/algorithm-functions.md#for_each) для последовательного вычисления числа. Затем в примере используется `parallel_for_each` алгоритм для параллельного выполнения одной и той же задачи. В этом примере в консоль также выводится время, необходимое на выполнение обоих вычислений.

[!code-cpp[concrt-parallel-count-primes#1](../../parallel/concrt/codesnippet/cpp/how-to-write-a-parallel-for-each-loop_1.cpp)]

В следующем примере показаны выходные данные, полученные на четырехпроцессорном компьютере.

```Output
serial version:
found 17984 prime numbers
took 6115 ms

parallel version:
found 17984 prime numbers
took 1653 ms
```

## <a name="compiling-the-code"></a>Компиляция кода

Чтобы скомпилировать код, скопируйте его и вставьте в проект Visual Studio или вставьте в файл с именем, `parallel-count-primes.cpp` а затем выполните следующую команду в окне командной строки Visual Studio.

> **cl.exe/EHsc Параллел-Каунт-примес. cpp**

## <a name="robust-programming"></a>Отказоустойчивость

Лямбда-выражение, которое в примере передается в `parallel_for_each` алгоритм, использует `InterlockedIncrement` функцию для включения параллельных итераций цикла для одновременного увеличения счетчика. Если вы используете такие функции `InterlockedIncrement` , как для синхронизации доступа к общим ресурсам, в коде можно представлять узкие места производительности. Чтобы исключить одновременный доступ к общим ресурсам, можно использовать механизм синхронизации без блокировки, например класс [Concurrency:: combinable](../../parallel/concrt/reference/combinable-class.md) . Пример использования `combinable` класса таким образом см. в разделе [как использовать комбинирование для повышения производительности](../../parallel/concrt/how-to-use-combinable-to-improve-performance.md).

## <a name="see-also"></a>См. также раздел

[Параллельные алгоритмы](../../parallel/concrt/parallel-algorithms.md)<br/>
[Функция parallel_for_each](reference/concurrency-namespace-functions.md#parallel_for_each)
