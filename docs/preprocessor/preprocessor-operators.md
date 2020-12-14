---
description: 'Дополнительные сведения: операторы препроцессора'
title: Операторы препроцессора
ms.date: 08/29/2019
helpviewer_keywords:
- preprocessor operators
- operators [C++], preprocessor
ms.assetid: 884126d1-0ce2-48b6-9e06-8a2d7c4a9656
ms.openlocfilehash: 960531a32dd8b4f834117fb01272e2ed45fecf92
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202097"
---
# <a name="preprocessor-operators"></a>Операторы препроцессора

В контексте Директивы используются четыре оператора, специфичных для препроцессора `#define` . В следующей таблице приведены сводные сведения о каждой из них. В следующих трех разделах рассматриваются преобразования в строку, преобразования в символы и вставки токенов. Дополнительные сведения об `defined` операторе см. [в разделе директивы #if, #elif, #else и #endif](../preprocessor/hash-if-hash-elif-hash-else-and-hash-endif-directives-c-cpp.md).

|Оператор|Действие|
|--------------|------------|
|[Оператор преобразования в строку (#)](../preprocessor/stringizing-operator-hash.md)|В результате его выполнения соответствующий аргумент заключается в двойные кавычки|
|[Оператор преобразования в символы (#@)](../preprocessor/charizing-operator-hash-at.md)|Заставляет соответствующий аргумент заключаться в одинарные кавычки и обрабатываться как символ (для конкретного приложения).|
|[Оператор вставки токена (##)](../preprocessor/token-pasting-operator-hash-hash.md)|Выполняет конкатенацию токенов, используемых в качестве фактических аргументов, для создания других токенов|
|[определенный оператор](../preprocessor/hash-if-hash-elif-hash-else-and-hash-endif-directives-c-cpp.md)|Упрощает написание составных выражений в некоторых директивах макросов|

## <a name="see-also"></a>См. также раздел

[Директивы препроцессора](../preprocessor/preprocessor-directives.md)\
[Предопределенные макросы](../preprocessor/predefined-macros.md)\
[Справочник по препроцессору c/c++](../preprocessor/c-cpp-preprocessor-reference.md)
