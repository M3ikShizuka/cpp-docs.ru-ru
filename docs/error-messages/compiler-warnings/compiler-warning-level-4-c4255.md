---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4255'
title: Предупреждение компилятора (уровень 4) C4255
ms.date: 11/04/2016
f1_keywords:
- C4255
helpviewer_keywords:
- C4255
ms.assetid: 2087b635-4b4c-4182-8a01-c26770d2bb88
ms.openlocfilehash: 31c5a121c944a65a0a5c3cd13d3e6201c3ad43a0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339160"
---
# <a name="compiler-warning-level-4-c4255"></a>Предупреждение компилятора (уровень 4) C4255

"функция": прототип функции не указан: преобразование "()" в "(void)"

Компилятору не удалось найти явный список аргументов для функции. Это предупреждение относится только к компилятору C.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

Следующий пример приводит к возникновению ошибки C4255:

```c
// C4255.c
// compile with: /W4 /WX
#pragma warning (default : 4255)

void f()  { // C4255
// try the following line instead
//void f(void) {
}

int main(int argc, char *argv[]) {
   f();
}
```
