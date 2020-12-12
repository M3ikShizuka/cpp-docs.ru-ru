---
description: 'Дополнительные сведения о: Ошибка компилятора C3389'
title: Ошибка компилятора C3389
ms.date: 11/04/2016
f1_keywords:
- C3389
helpviewer_keywords:
- C3389
ms.assetid: eaaffe17-23f2-413c-b1ad-f7220cfa1334
ms.openlocfilehash: b9fedf0993738d054cd5ded605d96001b3db13eb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97285504"
---
# <a name="compiler-error-c3389"></a>Ошибка компилятора C3389

> __declspec (*ключевое слово*) нельзя использовать с параметрами/clr: pure или/CLR: Сейф

## <a name="remarks"></a>Комментарии

**`/clr:pure`** **`/clr:safe`** Параметры компилятора и являются устаревшими в visual Studio 2015 и не поддерживаются в visual Studio 2017.

[`__declspec`](../../cpp/declspec.md)Используемый модификатор подразумевает состояние каждого процесса.  [`/clr:pure`](../../build/reference/clr-common-language-runtime-compilation.md) подразумевает состояние "на" [`appdomain`](../../cpp/appdomain.md) .  Таким образом, объявление переменной с модификатором *ключевого слова* **`__declspec`** и компиляция с помощью **`/clr:pure`** не допускается.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3389:

```cpp
// C3389.cpp
// compile with: /clr:pure /c
__declspec(dllexport) int g2 = 0;   // C3389
```
