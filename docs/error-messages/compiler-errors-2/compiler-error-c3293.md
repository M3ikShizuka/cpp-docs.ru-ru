---
description: 'Дополнительные сведения о: Ошибка компилятора C3293'
title: Ошибка компилятора C3293
ms.date: 07/21/2017
f1_keywords:
- C3293
helpviewer_keywords:
- C3293
ms.assetid: b772cf98-52e0-4e24-be23-1f5d87d999ac
ms.openlocfilehash: 5ba4256997eed12d3a380d5f3a4d1876da75fb8c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144642"
---
# <a name="compiler-error-c3293"></a>Ошибка компилятора C3293

"метод_доступа": используйте default для доступа к свойству по умолчанию (индексатору) для класса "тип"

Неправильный доступ к индексируемому свойству.  Дополнительные сведения см. в разделе [инструкции. Использование свойств в C++/CLI](../../dotnet/how-to-use-properties-in-cpp-cli.md) .

**Visual studio 2017 и более поздние версии**: в visual Studio 2015 и более ранних версиях компилятор в некоторых случаях по умолчанию неопределен как индексатор по умолчанию. Эту проблему удалось решить с использованием значения по умолчанию идентификатора для доступа к свойству. Возможное решение само по себе стало создавать проблемы после того, как значение умолчанию было представлено как ключевое слово в C++ 11. Поэтому в Visual Studio 2017 были исправлены ошибки, требующие обходного решения. Теперь компилятор выдает ошибку, когда значение по умолчанию используется для доступа к свойству по умолчанию для класса.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3293 в Visual Studio 2015 и более ранних версиях.

```cpp
// C3293.cpp
// compile with: /clr /c
using namespace System;
ref class IndexerClass {
public:
   // default indexer
   property int default[int] {
      int get(int index) { return 0; }
      void set(int index, int value) {}
   }
};

int main() {
   IndexerClass ^ ic = gcnew IndexerClass;
   ic->Item[0] = 21;   // C3293 in VS2015 OK in VS2017
   ic->default[0] = 21;   // OK in VS2015 and earlier

   String ^s = "Hello";
   wchar_t wc = s->Chars[0];   // C3293 in VS2015 OK in VS2017
   wchar_t wc2 = s->default[0];   // OK in VS2015 and earlier
   Console::WriteLine(wc2);
}
```
