---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4263'
title: Предупреждение компилятора (уровень 4) C4263
ms.date: 11/04/2016
f1_keywords:
- C4263
helpviewer_keywords:
- C4263
ms.assetid: daabb05d-ab56-460f-ab6c-c74d222ef649
ms.openlocfilehash: 7b7eb7fdf8e66ab5d09c8dc0f9511d3c88162084
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339150"
---
# <a name="compiler-warning-level-4-c4263"></a>Предупреждение компилятора (уровень 4) C4263

"функция": функция члена не переопределяет ни одной виртуальной функции члена базового класса

Определение функции класса имеет то же имя, что и виртуальная функция в базовом классе, но не имеет того же числа или типа аргументов. Это фактически скрывает виртуальную функцию в базовом классе.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

Следующий пример приводит к возникновению ошибки C4263:

```cpp
// C4263.cpp
// compile with: /W4
#pragma warning(default:4263)
#pragma warning(default:4264)
class B {
public:
   virtual void func();
};

class D : public B {
   void func(int);   // C4263
};

int main() {
}
```
