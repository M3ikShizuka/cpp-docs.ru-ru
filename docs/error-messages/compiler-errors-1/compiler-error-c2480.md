---
description: 'Дополнительные сведения о: Ошибка компилятора C2480'
title: Ошибка компилятора C2480
ms.date: 11/04/2016
f1_keywords:
- C2480
helpviewer_keywords:
- C2480
ms.assetid: 1a58d1c2-971b-4084-96fa-f94aa51c02f1
ms.openlocfilehash: 0c7f73b7e1aa205d38577602b93907309935b216
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316548"
---
# <a name="compiler-error-c2480"></a>Ошибка компилятора C2480

"идентификатор": "Thread" допустим только для элементов данных в статическом экстенте

Атрибут нельзя использовать `thread` с автоматической переменной, нестатическим элементом данных, параметром функции или объявлениями или определениями функций.

Используйте `thread` атрибут для глобальных переменных, статических элементов данных и локальных статических переменных.

Следующий пример приводит к возникновению ошибки C2480:

```cpp
// C2480.cpp
// compile with: /c
__declspec( thread ) void func();   // C2480
__declspec( thread ) static int i;   // OK
```
