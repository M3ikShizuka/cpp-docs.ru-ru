---
description: 'Дополнительные сведения о: предупреждение компилятора C4335'
title: Предупреждение компилятора C4335
ms.date: 11/04/2016
f1_keywords:
- C4335
helpviewer_keywords:
- C4335
ms.assetid: e66467ad-a10b-4438-8c7c-e8e8d11d39bb
ms.openlocfilehash: fc8f86036a299c41bc0cb1814b98372edc3b4d8f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97238314"
---
# <a name="compiler-warning-c4335"></a>Предупреждение компилятора C4335

Обнаружен формат файла Mac: преобразуйте исходный файл в формат DOS или UNIX

Символ завершения строки первой строки исходного файла имеет стиль Macintosh ("\r") в отличие от UNIX ("\n") или DOS ("\r\n").

Это предупреждение всегда выдается как ошибка.  Сведения о том, как отключить это предупреждение, см. в разделе [предупреждение](../../preprocessor/warning.md) pragma.  Кроме того, это предупреждение выдается только один раз для каждого компилируемого объекта. Таким образом, если существует несколько `#include` директив, которые указывают файлы в формате Macintosh, C4335 будет выдаваться только один раз.

Одним из способов создания файлов в формате Macintosh является использование **дополнительных параметров сохранения** (в меню **файл** ) в Visual Studio.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4335.

```cpp
// C4335 expected
#include "c4335.h"   // assume both include files are in Macintosh format
#include "c4335_2.h"
```
