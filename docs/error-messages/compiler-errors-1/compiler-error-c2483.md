---
description: 'Дополнительные сведения о: Ошибка компилятора C2483'
title: Ошибка компилятора C2483
ms.date: 09/15/2017
f1_keywords:
- C2483
helpviewer_keywords:
- C2483
ms.assetid: 5762b325-914b-442d-a604-e4617ba04038
ms.openlocfilehash: 5edafbbb0852eb622f34698421ce9a2b794f9209
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97123881"
---
# <a name="compiler-error-c2483"></a>Ошибка компилятора C2483

>"*идентификатор*": объект с конструктором или деструктором не может быть объявлен как "Thread"

Это сообщение об ошибке является устаревшим в Visual Studio 2015 и более поздних версиях. В предыдущих версиях переменные, объявленные с `thread` атрибутом, не могут быть инициализированы с помощью конструктора или другого выражения, которое требует вычисления во время выполнения. Для инициализации данных требуется статическое выражение `thread` .

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2483 в Visual Studio 2013 и более ранних версиях.

```cpp
// C2483.cpp
// compile with: /c
__declspec(thread) struct A {
   A(){}
   ~A(){}
} aa;   // C2483 error

__declspec(thread) struct B {} b;   // OK
```

## <a name="see-also"></a>См. также раздел

[поток](../../cpp/thread.md)
