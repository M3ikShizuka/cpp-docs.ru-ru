---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4917'
title: Предупреждение компилятора (уровень 1) C4917
ms.date: 11/04/2016
f1_keywords:
- C4917
helpviewer_keywords:
- C4917
ms.assetid: c05e2610-4a5d-4f4b-a99b-c15fd7f1d5f1
ms.openlocfilehash: b85d9dced285eade22cf6b8ff61657cd53703b88
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97291432"
---
# <a name="compiler-warning-level-1-c4917"></a>Предупреждение компилятора (уровень 1) C4917

"декларатор": GUID может быть связан только с классом, интерфейсом или пространством имен

Определяемая пользователем структура, отличная от [класса](../../cpp/class-cpp.md), [интерфейса](../../cpp/interface.md)или [пространства имен](../../cpp/namespaces-cpp.md) , не может иметь идентификатор GUID.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

## <a name="example"></a>Пример

Следующий пример кода приводит к возникновению ошибки C4917:

```cpp
// C4917.cpp
// compile with: /W1
#pragma warning(default : 4917)
__declspec(uuid("00000000-0000-0000-0000-000000000001")) struct S
{
} s;   // C4917, don't put uuid on a struct

int main()
{
}
```
