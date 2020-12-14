---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4532'
title: Предупреждение компилятора (уровень 1) C4532
ms.date: 11/04/2016
f1_keywords:
- C4532
helpviewer_keywords:
- C4532
ms.assetid: 4e2a286a-d233-4106-9f65-29be1a94ca02
ms.openlocfilehash: 9468ca1242397289c832fec28d71cf245c6c8a5f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294812"
---
# <a name="compiler-warning-level-1-c4532"></a>Предупреждение компилятора (уровень 1) C4532

"продолжить": переход из __finally блока/финалли имеет неопределенное поведение во время обработки завершения

Компилятор обнаружил одно из следующих ключевых слов:

- [continue](../../cpp/continue-statement-cpp.md)

- [break](../../cpp/break-statement-cpp.md)

- [goto](../../cpp/goto-statement-cpp.md)

причиной перехода из [__finally](../../cpp/try-finally-statement.md) или [finally](../../dotnet/finally.md) в случае аварийного завершения.

Если возникает исключение, а во время дефрагментации стека в процессе выполнения обработчиков завершения ( **`__finally`** блоки finally) и код выходит за пределы **`__finally`** блока до **`__finally`** завершения блока, поведение не определено. Управление может не вернуться в код очистки, поэтому исключение может быть неправильно обработано.

Если необходимо переходить к **`__finally`** блоку, сначала проверьте наличие аномального завершения.

Следующий пример приводит к возникновению ошибки C4532; просто закомментируйте инструкции перехода, чтобы устранить предупреждения.

```cpp
// C4532.cpp
// compile with: /W1
// C4532 expected
int main() {
   int i;
   for (i = 0; i < 10; i++) {
      __try {
      } __finally {
         // Delete the following line to resolve.
         continue;
      }

      __try {
      } __finally {
         // Delete the following line to resolve.
         break;
      }
   }
}
```
