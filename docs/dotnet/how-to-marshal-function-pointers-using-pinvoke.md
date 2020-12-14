---
description: 'Дополнительные сведения о: инструкции: маршалирование указателей функций с помощью PInvoke'
title: Практическое руководство. Указатели функций маршалирования, использующие PInvoke
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- data marshaling [C++], callbacks and delegates
- interop [C++], callbacks and delegates
- platform invoke [C++], callbacks and delegates
- marshaling [C++], callbacks and delegates
ms.assetid: dcf396fd-a91d-49c0-ab0b-1ea160668a89
ms.openlocfilehash: bfe3f669cf023ed914bdccb3ae15ccafefbb49c2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97302586"
---
# <a name="how-to-marshal-function-pointers-using-pinvoke"></a>Практическое руководство. Указатели функций маршалирования, использующие PInvoke

В этом разделе объясняется, как можно использовать управляемые делегаты вместо указателей на функции при взаимодействии с неуправляемыми функциями с помощью функций .NET Framework P/Invoke. Тем не менее Visual C++ программистам рекомендуется использовать функции взаимодействия C++ (по возможности), поскольку P/Invoke предоставляет небольшие отчеты об ошибках во время компиляции, не является типобезопасным и может быть утомительным для реализации. Если неуправляемый интерфейс API упакован как DLL и исходный код недоступен, то единственным вариантом является P/Invoke. В противном случае см. следующие разделы:

- [Использование взаимодействия C++ (неявный PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)

- [Инструкции. маршалирование обратных вызовов и делегатов с помощью взаимодействия C++](../dotnet/how-to-marshal-callbacks-and-delegates-by-using-cpp-interop.md)

Неуправляемые интерфейсы API, принимающие указатели на функции в качестве аргументов, можно вызывать из управляемого кода с помощью управляемого делегата вместо указателя на функцию в машинном коде. Компилятор автоматически маршалирует делегат в неуправляемые функции в качестве указателя функции и вставляет необходимый управляемый и неуправляемый код перехода.

## <a name="example"></a>Пример

Следующий код состоит из неуправляемого и управляемого модуля. Неуправляемый модуль — это библиотека DLL, которая определяет функцию с именем Такескаллбакк, которая принимает указатель на функцию. Этот адрес используется для выполнения функции.

Управляемый модуль определяет делегат, который маршалируется в машинный код в качестве указателя функции, и использует <xref:System.Runtime.InteropServices.DllImportAttribute> атрибут для предоставления машинной функции такескаллбакк управляемому коду. В функции Main создается экземпляр делегата, который передается функции Такескаллбакк. Выходные данные программы показывают, что эта функция выполняется собственной функцией Такескаллбакк.

Управляемая функция подавляет сборку мусора для управляемого делегата, чтобы предотвратить повторное размещение делегата .NET Framework сборки мусора во время выполнения собственной функции.

```cpp
// TraditionalDll5.cpp
// compile with: /LD /EHsc
#include <iostream>
#define TRADITIONALDLL_EXPORTS
#ifdef TRADITIONALDLL_EXPORTS
#define TRADITIONALDLL_API __declspec(dllexport)
#else
#define TRADITIONALDLL_API __declspec(dllimport)
#endif

extern "C" {
   /* Declare an unmanaged function type that takes two int arguments
      Note the use of __stdcall for compatibility with managed code */
   typedef int (__stdcall *CALLBACK)(int);
   TRADITIONALDLL_API int TakesCallback(CALLBACK fp, int);
}

int TakesCallback(CALLBACK fp, int n) {
   printf_s("[unmanaged] got callback address, calling it...\n");
   return fp(n);
}
```

```cpp
// MarshalDelegate.cpp
// compile with: /clr
using namespace System;
using namespace System::Runtime::InteropServices;

public delegate int GetTheAnswerDelegate(int);
public value struct TraditionalDLL {
   [DllImport("TraditionalDLL5.dll")]
   static public int TakesCallback(GetTheAnswerDelegate^ pfn, int n);
};

int GetNumber(int n) {
   Console::WriteLine("[managed] callback!");
   static int x = 0;
   ++x;
   return x + n;
}

int main() {
   GetTheAnswerDelegate^ fp = gcnew GetTheAnswerDelegate(GetNumber);
   pin_ptr<GetTheAnswerDelegate^> pp = &fp;
   Console::WriteLine("[managed] sending delegate as callback...");

   int answer = TraditionalDLL::TakesCallback(fp, 42);
}
```

Обратите внимание, что ни одна часть библиотеки DLL не предоставляется управляемому коду с помощью традиционной директивы #include. На самом деле библиотека DLL доступна только во время выполнения, поэтому проблемы с функциями, импортированными с помощью, <xref:System.Runtime.InteropServices.DllImportAttribute> не будут обнаружены во время компиляции.

## <a name="see-also"></a>См. также раздел

[Использование явного вызова PInvoke в C++ (атрибут DllImport)](../dotnet/using-explicit-pinvoke-in-cpp-dllimport-attribute.md)
