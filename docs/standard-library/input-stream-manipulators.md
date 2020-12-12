---
description: 'Дополнительные сведения о: входные манипуляторы потока'
title: Манипуляторы входных потоков
ms.date: 11/04/2016
helpviewer_keywords:
- input streams, manipulators
- input stream objects
ms.assetid: 0addcacb-7b7b-4d70-9775-a59abc400fb3
ms.openlocfilehash: 3da317a9e01652debe0114cfbde284ec0edf6db3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323993"
---
# <a name="input-stream-manipulators"></a>Манипуляторы входных потоков

Многие манипуляторы, такие как [setprecision](../standard-library/iomanip-functions.md#setprecision), определены для `ios` класса и поэтому применяются к входным потокам. Однако некоторые манипуляторы фактически влияют на объекты потока ввода. Наиболее важными из них являются манипуляторы основания системы счисления `dec`, `oct` и `hex`, которые определяют базу преобразования, используемую с числами из входного потока.

При извлечении манипулятор `hex` позволяет обрабатывать различные форматы входных данных. Например, c C, 0xc, 0xC, 0Xc и 0XC интерпретируются как десятичное целое число 12. Любой символ, отличный от цифр от 0 до 9, букв от A до F, букв от a до f, x и X, завершает числовое преобразование. Таким образом, последовательность `"124n5"` преобразуется в число 124 с заданными битом [basic_ios::fail](../standard-library/basic-ios-class.md#fail).

## <a name="see-also"></a>См. также раздел

[Входные потоки](../standard-library/input-streams.md)
