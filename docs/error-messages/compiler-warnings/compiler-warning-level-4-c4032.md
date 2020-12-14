---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4032'
title: Предупреждение компилятора (уровень 4) C4032
ms.date: 11/04/2016
f1_keywords:
- C4032
helpviewer_keywords:
- C4032
ms.assetid: 70dd0c85-0239-43f9-bb06-507f6a57d206
ms.openlocfilehash: 1c150bff398bbd2d6e5f1a8d21211f4c6b4cb6bd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97262104"
---
# <a name="compiler-warning-level-4-c4032"></a>Предупреждение компилятора (уровень 4) C4032

формальный параметр "число" имеет другой тип при повышении уровня

Тип параметра несовместим с использованием специальных предложений по умолчанию с типом в предыдущем объявлении.

Это ошибка в ANSI C ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) и предупреждение в разделе расширения Майкрософт (/Ze).

## <a name="example"></a>Пример

```c
// C4032.c
// compile with: /W4
void func();
void func(char);   // C4032, char promotes to int

int main()
{
}
```
