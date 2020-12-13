---
description: 'Дополнительные сведения о: Ошибка компилятора C3284'
title: Ошибка компилятора C3284
ms.date: 11/04/2016
f1_keywords:
- C3284
helpviewer_keywords:
- C3284
ms.assetid: e582f316-e9db-4d27-9c70-fdfa737a9d5f
ms.openlocfilehash: 1c899a3c6fff539dc2676ca685d892b906269253
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339239"
---
# <a name="compiler-error-c3284"></a>Ошибка компилятора C3284

ограничения для универсального параметра "параметр" функции "функция" должны соответствовать ограничениям для универсального параметра "параметр" функции "функция"

Виртуальная универсальная функция должна использовать те же ограничения, что и виртуальная функция с тем же именем и набором аргументов в базовом классе.

Следующий пример приводит к возникновению ошибки C3284:

```cpp
// C3284.cpp
// compile with: /clr /c
// C3284 expected
public interface class IGettable {
   int Get();
};

public interface class B {
   generic<typename T>
   where T : IGettable
   virtual int mf(T t);
};

public ref class D : public B {
public:
   generic<typename T>
   // Uncomment the following line to resolve.
   // where T : IGettable
   virtual int mf(T t) {
      return 4;
   }
};
```
