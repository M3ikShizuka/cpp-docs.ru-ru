---
description: 'Дополнительные сведения о: Неустранимая ошибка C1019'
title: Неустранимая ошибка C1019
ms.date: 11/04/2016
f1_keywords:
- C1019
helpviewer_keywords:
- C1019
ms.assetid: c4f8968b-bc62-4200-b3ca-69d06c163236
ms.openlocfilehash: d11a4300b29e497fef2f148d07963997586781ec
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316392"
---
# <a name="fatal-error-c1019"></a>Неустранимая ошибка C1019

непредвиденный #else

Директива `#else` встречается за пределами конструкции `#if`, `#ifdef`или `#ifndef` . Используйте `#else` только в одной из этих конструкций.

При компиляции следующего примера возникнет ошибка C1019:

```cpp
// C1019.cpp
#else   // C1019
#endif

int main() {}
```

Возможное решение:

```cpp
// C1019b.cpp
#if 1
#else
#endif

int main() {}
```
