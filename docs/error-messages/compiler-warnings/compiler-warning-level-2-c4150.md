---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 2) C4150'
title: Предупреждение компилятора (уровень 2) C4150
ms.date: 11/04/2016
f1_keywords:
- C4150
helpviewer_keywords:
- C4150
ms.assetid: ff1760ec-0d9f-4d45-b797-94261624becf
ms.openlocfilehash: 9b0296b94bbb2aab18b579898f053e002397c04e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97177254"
---
# <a name="compiler-warning-level-2-c4150"></a>Предупреждение компилятора (уровень 2) C4150

удаление указателя на неполный тип "тип"; деструктор не вызван

**`delete`** Оператор вызывается для удаления типа, который был объявлен, но не определен, поэтому компилятору не удается найти деструктор.

Следующий пример приводит к возникновению ошибки C4150:

```cpp
// C4150.cpp
// compile with: /W2
class  IncClass;

void NoDestruct( IncClass* pIncClass )
{
   delete pIncClass;
} // C4150, define class to resolve

int main()
{
}
```
