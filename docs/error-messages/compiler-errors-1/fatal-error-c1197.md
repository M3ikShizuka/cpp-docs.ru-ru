---
description: 'Дополнительные сведения о: Неустранимая ошибка C1197'
title: Неустранимая ошибка C1197
ms.date: 11/04/2016
f1_keywords:
- C1197
helpviewer_keywords:
- C1197
ms.assetid: 22b801b7-e792-41f6-a461-973c03c69f25
ms.openlocfilehash: c61cbd71fa8f17dc787fd9ee5eabd0f073aafb39
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97268175"
---
# <a name="fatal-error-c1197"></a>Неустранимая ошибка C1197

невозможно сослаться на "mscorlib.dll_1", так как программа уже ссылалась на "mscorlib.dll_2"

Компилятор соответствует версии среды CLR.  Однако была предпринята попытка сослаться на версию файла среды CLR, созданную из предыдущей версии.

Чтобы устранить эту ошибку, следует ссылаться только на файлы из версии среды CLR, поставляемой с версией Visual C++, с которой выполняется компиляция.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C1197:

```cpp
// C1197.cpp
// compile with: /clr /c
// processor: x86
#using "C:\Windows\Microsoft.NET\Framework\v1.1.4322\mscorlib.dll"   // C1197
// try the following line instead
// #using "mscorlib.dll"
```
