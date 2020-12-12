---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 2) C4094'
title: Предупреждение компилятора (уровень 2) C4094
ms.date: 11/04/2016
f1_keywords:
- C4094
helpviewer_keywords:
- C4094
ms.assetid: e68929fb-3a1c-4be7-920b-d5f79f534f99
ms.openlocfilehash: 63c554703c1eb6f7ecb831d1046641a0cde2094a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326535"
---
# <a name="compiler-warning-level-2-c4094"></a>Предупреждение компилятора (уровень 2) C4094

без тега "token" не объявлен ни один символ

Компилятор обнаружил пустое объявление с использованием структуры, объединения или класса без тегов. Объявление игнорируется.

## <a name="example"></a>Пример

```cpp
// C4094.cpp
// compile with: /W2
struct
{
};   // C4094

int main()
{
}
```

Это условие приводит к ошибке в режиме совместимости ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).
