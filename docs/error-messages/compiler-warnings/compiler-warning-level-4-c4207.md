---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4207'
title: Предупреждение компилятора (уровень 4) C4207
ms.date: 11/04/2016
f1_keywords:
- C4207
helpviewer_keywords:
- C4207
ms.assetid: f4e09e3e-ac87-4489-8e3f-c8f76b82e721
ms.openlocfilehash: fe442f71789533227a68a2f9059291de207e277b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97173224"
---
# <a name="compiler-warning-level-4-c4207"></a>Предупреждение компилятора (уровень 4) C4207

использовано нестандартное расширение: Расширенная форма инициализатора

С помощью расширений Майкрософт (/Ze) можно инициализировать неразмерный массив, **`char`** используя строку внутри фигурных скобок.

## <a name="example"></a>Пример

```c
// C4207.c
// compile with: /W4
char c[] = { 'a', 'b', "cdefg" }; // C4207

int main()
{
}
```

Такие инициализации недопустимы в режиме совместимости ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).
