---
description: 'Дополнительные сведения: наконец'
title: finally
ms.date: 11/04/2016
helpviewer_keywords:
- finally keyword [C++]
ms.assetid: b55f3c8e-1af0-43e8-bcfb-99c3685d2578
ms.openlocfilehash: 039c3fab7854d045c9b4917d2a0bc9f01fdc61a3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97252159"
---
# <a name="finally"></a>finally

Помимо **`try`** **`catch`** предложений и, обработка исключений CLR поддерживает **`finally`** предложение. Семантика идентична **`__finally`** блоку в структурированной обработке исключений (SEH). **`__finally`** Блок может следовать за **`try`** **`catch`** блоком или.

## <a name="remarks"></a>Комментарии

Целью этого **`finally`** блока является очистка всех ресурсов, оставшихся после возникновения исключения. Обратите внимание, что **`finally`** блок всегда выполняется, даже если исключение не было создано. **`catch`** Блок выполняется только в том случае, если управляемое исключение создается в связанном **`try`** блоке.

`finally` контекстно-зависимое ключевое слово; Дополнительные сведения см. в разделе [контекстно-зависимые ключевые слова](../extensions/context-sensitive-keywords-cpp-component-extensions.md) .

## <a name="example"></a>Пример

В следующем примере показан простой **`finally`** блок:

```cpp
// keyword__finally.cpp
// compile with: /clr
using namespace System;

ref class MyException: public System::Exception{};

void ThrowMyException() {
   throw gcnew MyException;
}

int main() {
   try {
      ThrowMyException();
   }
   catch ( MyException^ e ) {
      Console::WriteLine(  "in catch" );
      Console::WriteLine( e->GetType() );
   }
   finally {
      Console::WriteLine(  "in finally" );
   }
}
```

```Output
in catch
MyException
in finally
```

## <a name="see-also"></a>См. также раздел

[Обработка исключений](../extensions/exception-handling-cpp-component-extensions.md)
