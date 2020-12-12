---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4218'
title: Предупреждение компилятора (уровень 4) C4218
ms.date: 11/04/2016
f1_keywords:
- C4218
helpviewer_keywords:
- C4218
ms.assetid: d6c3cd90-4518-49e9-ae86-4ba9e2761d98
ms.openlocfilehash: 76fc53a5b290a55c73fe036e2fc02b7a1afedd23
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97266420"
---
# <a name="compiler-warning-level-1-c4218"></a>Предупреждение компилятора (уровень 4) C4218

использовано нестандартное расширение: необходимо указать по крайней мере класс хранения или тип

Используя расширения Майкрософт по умолчанию (/Ze), можно объявить переменную без указания типа или класса хранения. Тип по умолчанию — **`int`** .

## <a name="example"></a>Пример

```cpp
// C4218.c
// compile with: /W4
i;  // C4218

int main()
{
}
```

Такие объявления недопустимы в режиме совместимости ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).
