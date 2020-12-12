---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4221'
title: Предупреждение компилятора (уровень 4) C4221
ms.date: 11/04/2016
f1_keywords:
- C4221
helpviewer_keywords:
- C4221
ms.assetid: 8532bd68-54dc-4526-8597-f61dcb0a0129
ms.openlocfilehash: 4632b075dfb6a7c1895415a253c70f5b4fd4f278
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97164280"
---
# <a name="compiler-warning-level-4-c4221"></a>Предупреждение компилятора (уровень 4) C4221

использовано нестандартное расширение: "идентификатор": невозможно инициализировать с помощью адреса автоматической переменной

С помощью расширений Майкрософт по умолчанию (/Ze) можно инициализировать агрегатный тип (**массив**, **`struct`** или **`union`** ) с адресом локальной (автоматической) переменной.

## <a name="example"></a>Пример

```c
// C4221.c
// compile with: /W4
struct S
{
   int *i;
};

void func()
{
   int j;
   struct S s1 = { &j };   // C4221
}

int main()
{
}
```

Такие инициализации недопустимы в режиме совместимости ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).
