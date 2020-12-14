---
description: 'Дополнительные сведения о: Ошибка компилятора C3848'
title: Ошибка компилятора C3848
ms.date: 11/04/2016
f1_keywords:
- C3848
helpviewer_keywords:
- C3848
ms.assetid: 32d3ccef-01ec-4f8b-bbff-fb9b1a76b4c4
ms.openlocfilehash: 8bd81f59927dd1b34c23148dd1e9bd69ec715609
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97255383"
---
# <a name="compiler-error-c3848"></a>Ошибка компилятора C3848

выражение HAVING типа "тип" потеряет некоторые квалификаторы const-volatile для вызова "Function"

Переменная с указанным типом const константы может вызывать только функции-члены, определенные с теми же или большими квалификациями const-volatile.

Следующие примеры создают C3848:

```cpp
// C3848.cpp
void glbFunc1()
{
}

typedef void (* pFunc1)();

struct S3
{
   operator pFunc1() // const
   {
      return &glbFunc1;
   }
};

int main()
{
   const S3 s3;
   s3();   // C3848, uncomment const qualifier
}
```
