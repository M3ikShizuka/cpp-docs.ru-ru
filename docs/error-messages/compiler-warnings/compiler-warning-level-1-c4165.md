---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4165'
title: Предупреждение компилятора (уровень 1) C4165
ms.date: 11/04/2016
f1_keywords:
- C4165
helpviewer_keywords:
- C4165
ms.assetid: f5bed515-2290-4f88-8dab-b45d95fe26ef
ms.openlocfilehash: 7b82db7421493b1687b35e61da988b68a577e8a5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97267044"
---
# <a name="compiler-warning-level-1-c4165"></a>Предупреждение компилятора (уровень 1) C4165

Выполняется преобразование "HRESULT" в "bool"; Вы уверены, что это нужно?

При использовании HRESULT в операторе [If](../../cpp/if-else-statement-cpp.md) значение HRESULT будет преобразовано в [bool](../../cpp/bool-cpp.md) , если явно не проверить переменную как HRESULT. Это предупреждение отключено по умолчанию.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4165

```cpp
// C4165.cpp
// compile with: /W1
#include <windows.h>
#pragma warning(1:4165)

extern HRESULT hr;
int main() {
   if (hr) {
   // try either of the following ...
   // if (FAILED(hr)) { // C4165 expected
   // if (hr != S_OK) {
   }
}
```
