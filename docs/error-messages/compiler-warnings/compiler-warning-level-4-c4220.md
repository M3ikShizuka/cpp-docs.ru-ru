---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4220'
title: Предупреждение компилятора (уровень 4) C4220
ms.date: 11/04/2016
f1_keywords:
- C4220
helpviewer_keywords:
- C4220
ms.assetid: aba18868-825f-4763-9af6-3296406a80e4
ms.openlocfilehash: fd5378fd1e685b2cc6e730c2cff87fcdb041aaa8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330631"
---
# <a name="compiler-warning-level-4-c4220"></a>Предупреждение компилятора (уровень 4) C4220

varargs соответствует оставшимся параметрам

В расширениях Майкрософт по умолчанию (/Ze) указатель на функцию соответствует указателю на функцию с аналогичным, но переменной, аргументами.

## <a name="example"></a>Пример

```c
// C4220.c
// compile with: /W4

int ( *pFunc1) ( int a, ... );
int ( *pFunc2) ( int a, int b);

int main()
{
   if ( pFunc1 != pFunc2 ) {};  // C4220
}
```

Такие указатели не соответствуют по ANSI-совместимости ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).
