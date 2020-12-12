---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4266'
title: Предупреждение компилятора (уровень 4) C4266
ms.date: 11/04/2016
f1_keywords:
- C4266
helpviewer_keywords:
- C4266
ms.assetid: 90ec5f5b-3451-4c16-bb1b-c30a626bdaa0
ms.openlocfilehash: 173e7da734a1bd94ccee9684bc2400c020dfc76c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97285179"
---
# <a name="compiler-warning-level-4-c4266"></a>Предупреждение компилятора (уровень 4) C4266

"функция": нет доступных переопределений для виртуальной функции члена из базового типа "тип"; функция скрыта

Производный класс не переопределяет все перегрузки виртуальной функции.

Это предупреждение отключено по умолчанию.  Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

Следующий пример приводит к возникновению ошибки C4266:

```cpp
// C4266.cpp
// compile with: /W4 /c
#pragma warning (default : 4266)
class Engine {
public:
   virtual void OnException(int&,int);
   virtual void OnException(int&,int&,int);
};

class LocalBinding : private Engine {
   virtual void OnException(int&,int);
};   // C4266
```

Возможное решение:

```cpp
// C4266b.cpp
// compile with: /W4 /c
#pragma warning (default : 4266)
class Engine {
public:
   virtual void OnException(int&,int);
   virtual void OnException(int&,int&,int);
};

class LocalBinding : private Engine {
   virtual void OnException(int&,int);
   virtual void OnException(int&, int&, int);
};
```
