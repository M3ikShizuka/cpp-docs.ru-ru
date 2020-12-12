---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4214'
title: Предупреждение компилятора (уровень 4) C4214
ms.date: 11/04/2016
f1_keywords:
- C4214
helpviewer_keywords:
- C4214
ms.assetid: 9b8db279-1f12-4a6b-a923-2db22acd1947
ms.openlocfilehash: afc3f425f0d37b3fb3063d18cb514336271a30ae
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297308"
---
# <a name="compiler-warning-level-4-c4214"></a>Предупреждение компилятора (уровень 4) C4214

нестандартное расширение: типы битовых полей, отличные от int

С расширениями Майкрософт по умолчанию (/Ze) битовые элементы структуры могут иметь любой целочисленный тип.

## <a name="example"></a>Пример

```c
// C4214.c
// compile with: /W4
struct bitfields
{
   unsigned short j:4;  // C4214
};

int main()
{
}
```

Такие битовые поля недопустимы в режиме совместимости ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).
