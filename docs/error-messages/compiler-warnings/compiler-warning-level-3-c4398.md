---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4398'
title: Предупреждение компилятора (уровень 3) C4398
ms.date: 11/04/2016
f1_keywords:
- C4398
helpviewer_keywords:
- C4398
ms.assetid: b6221432-9fed-4272-a547-a73f587904e6
ms.openlocfilehash: ea88f81e44fe0520cd096e1904c49a306863496a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97160432"
---
# <a name="compiler-warning-level-3-c4398"></a>Предупреждение компилятора (уровень 3) C4398

> "*переменная*": глобальный объект для каждого процесса может работать неправильно с несколькими доменами приложений; Попробуйте использовать __declspec (AppDomain)

## <a name="remarks"></a>Комментарии

Виртуальная функция с соглашением о вызове [__clrcall](../../cpp/clrcall.md) в собственном типе приводит к созданию виртуальной таблицы для каждого приложения. Такая переменная может неправильно исправляться при использовании в нескольких доменах приложений.

Это предупреждение можно устранить, явно пометив переменную `__declspec(appdomain)` . В версиях Visual Studio до Visual Studio 2017 можно устранить это предупреждение, выполнив компиляцию с **параметром/clr: pure**, который по умолчанию делает глобальные переменные для каждого AppDomain. Параметр компилятора **/clr: pure** является устаревшим в visual Studio 2015 и не поддерживается в visual Studio 2017.

Дополнительные сведения см. в разделе [AppDomain](../../cpp/appdomain.md) и [домены приложений и Visual C++](../../dotnet/application-domains-and-visual-cpp.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4398.

```cpp
// C4398.cpp
// compile with: /clr /W3 /c
struct S {
   virtual void f( System::String ^ );   // String^ parameter makes function __clrcall
};

S glob_s;   // C4398
__declspec(appdomain) S glob_s2;   // OK
```
