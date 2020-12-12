---
description: 'Дополнительные сведения о: Ошибка компилятора C2432'
title: Ошибка компилятора C2432
ms.date: 11/04/2016
f1_keywords:
- C2432
helpviewer_keywords:
- C2432
ms.assetid: 0e3326e8-cab1-45a5-b48d-61edd33793e8
ms.openlocfilehash: 392108e0fd16952bc8bcf43682dc163c664171ea
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190020"
---
# <a name="compiler-error-c2432"></a>Ошибка компилятора C2432

Недопустимая ссылка на 16-разрядные данные в "identifier"

16-разрядный регистр используется в качестве индекса или базового регистра. Компилятор не поддерживает ссылки на 16-разрядные данные. 16-разрядные регистры не могут использоваться в качестве индексов или базовых регистров при компиляции для 32-разрядного кода.

Следующий пример приводит к возникновению ошибки C2432:

```cpp
// C2432.cpp
// processor: x86
int main() {
   _asm mov eax, DWORD PTR [bx]   // C2432
}
```
