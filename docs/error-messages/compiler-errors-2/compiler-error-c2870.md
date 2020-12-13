---
description: 'Дополнительные сведения о: Ошибка компилятора C2870'
title: Ошибка компилятора C2870
ms.date: 11/04/2016
f1_keywords:
- C2870
helpviewer_keywords:
- C2870
ms.assetid: 80523ee9-1fd3-4dc4-8a77-5083deb99066
ms.openlocfilehash: 74e7f2de5cfbb5aca6bd653f5711b989de4ef326
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333768"
---
# <a name="compiler-error-c2870"></a>Ошибка компилятора C2870

"имя": определение пространства имен должно находиться либо в области файла, либо непосредственно в пределах другого определения пространства имен

Задано `name` Неправильное пространство имен. Пространства имен должны быть определены в области видимости файла (вне всех блоков и классов) или непосредственно в другом пространстве имен.

Следующий пример приводит к возникновению ошибки C2870:

```cpp
// C2870.cpp
// compile with: /c
int main() {
   namespace A { int i; };   // C2870
}
```
