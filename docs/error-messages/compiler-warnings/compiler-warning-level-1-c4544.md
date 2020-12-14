---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4544'
title: Предупреждение компилятора (уровень 1) C4544
ms.date: 11/04/2016
f1_keywords:
- C4544
helpviewer_keywords:
- C4544
ms.assetid: 11ee04df-41ae-435f-af44-881e801315a8
ms.openlocfilehash: cd7d4dddd43a8cac0ce4eb5115dbbadad3d56103
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294760"
---
# <a name="compiler-warning-level-1-c4544"></a>Предупреждение компилятора (уровень 1) C4544

declaration: аргумент шаблона по умолчанию пропускается в этом объявлении шаблона

Аргумент шаблона по умолчанию указан в неправильном месте и был пропущен. Аргумент шаблона по умолчанию для шаблона класса может быть указан только в объявлении или определении шаблона класса, но не в члене шаблона класса.

В этом примере показано возникновение ошибки C4545, а в следующем примере приводятся сведения по ее устранению.

```cpp
// C4544.cpp
// compile with: /W1 /LD
template <class T>
struct S
{
   template <class T1>
      struct S1;
   void f();
};

template <class T=int>
template <class T1>
struct S<T>::S1 {};   // C4544
```

В этом примере параметр по умолчанию применяется к шаблону класса `S`:

```cpp
// C4544b.cpp
// compile with: /LD
template <class T = int>
struct S
{
   template <class T1>
      struct S1;
   void f();
};

template <class T>
template <class T1>
struct S<T>::S1 {};
```
