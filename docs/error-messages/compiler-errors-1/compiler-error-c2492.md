---
description: 'Дополнительные сведения о: Ошибка компилятора C2492'
title: Ошибка компилятора C2492
ms.date: 11/04/2016
f1_keywords:
- C2492
helpviewer_keywords:
- C2492
ms.assetid: 8c44c9bb-c366-4fe5-a0ab-882e38608aaa
ms.openlocfilehash: ef31b2136a2cfc0422832899dba14ffb3108d965
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97283683"
---
# <a name="compiler-error-c2492"></a>Ошибка компилятора C2492

"*переменная*": данные с длительностью хранилища потоков могут не иметь интерфейс DLL

Переменная объявляется с помощью атрибута [Thread](../../cpp/thread.md) и интерфейса DLL. Адрес `thread` переменной неизвестен до времени выполнения, поэтому он не может быть связан с импортом или экспортом DLL.

Следующий пример приводит к возникновению ошибки C2492:

```cpp
// C2492.cpp
// compile with: /c
class C {
public:
   char   ch;
};

__declspec(dllexport) __declspec(thread) C c_1;   // C2492
__declspec(thread) C c_1;   // OK
```
