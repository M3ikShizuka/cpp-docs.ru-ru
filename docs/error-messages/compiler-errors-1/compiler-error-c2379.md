---
description: 'Дополнительные сведения о: Ошибка компилятора C2379'
title: Ошибка компилятора C2379
ms.date: 11/04/2016
f1_keywords:
- C2379
helpviewer_keywords:
- C2379
ms.assetid: 37dc3015-a4af-4341-bbf3-da6150df7e51
ms.openlocfilehash: 4b278040107a026ffd5f7bee79e709519647cb54
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174719"
---
# <a name="compiler-error-c2379"></a>Ошибка компилятора C2379

номер формального параметра имеет другой тип при повышении уровня

Тип указанного параметра несовместим с использованием специальных предложений по умолчанию с типом в предыдущем объявлении. Это ошибка в ANSI C ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) и предупреждение с расширениями Майкрософт (**/Ze**).

Следующий пример приводит к возникновению ошибки C2379:

```c
// C2379.c
// compile with: /Za
void func();
void func(char);   // C2379, char promotes to int
```
