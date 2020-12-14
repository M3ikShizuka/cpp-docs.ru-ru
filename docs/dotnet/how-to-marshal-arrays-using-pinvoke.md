---
description: Дополнительные сведения см. в статье как маршалировать массивы с помощью PInvoke.
title: Практическое руководство. Маршалинг массивов с помощью службы PInvoke
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- marshaling [C++], arrays
- platform invoke [C++], arrays
- interop [C++], arrays
- data marshaling [C++], arrays
ms.assetid: a1237797-a2da-4df4-984a-6333ed3af406
ms.openlocfilehash: 90fd7b2cbefe2fb3621f512d49fbc088240922a1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97258229"
---
# <a name="how-to-marshal-arrays-using-pinvoke"></a>Практическое руководство. Маршалинг массивов с помощью службы PInvoke

В этом разделе объясняется, как можно вызывать собственные функции, которые принимают строки в стиле C, используя строковый тип CLR <xref:System.String> с помощью .NET Framework поддержки вызова неуправляемого кода. Visual C++ программистам рекомендуется использовать функции взаимодействия C++ (если это возможно), поскольку P/Invoke предоставляет небольшие отчеты об ошибках во время компиляции, не является типобезопасным и может быть утомительным для реализации. Если неуправляемый интерфейс API упакован как DLL и исходный код недоступен, то единственным вариантом (в противном случае см. раздел [использование взаимодействия C++ (неявный PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)).

## <a name="example"></a>Пример

Поскольку собственные и управляемые массивы размещаются в памяти по-разному, для их успешной передачи между управляемой и неуправляемой границей требуется преобразование или маршалирование. В этом разделе показано, как массив простых (блитабле) элементов можно передать в собственные функции из управляемого кода.

Как и в случае с обобщением управляемого и неуправляемого данных в целом, <xref:System.Runtime.InteropServices.DllImportAttribute> атрибут используется для создания управляемой точки входа для каждой собственной функции, которая будет использоваться. В случае с функциями, принимающими в качестве аргументов массивы, <xref:System.Runtime.InteropServices.MarshalAsAttribute> необходимо также использовать атрибут, чтобы указать компилятору, каким образом данные будут маршалированы. В следующем примере <xref:System.Runtime.InteropServices.UnmanagedType> перечисление используется для указания того, что управляемый массив будет упакован как массив в стиле C.

Следующий код состоит из неуправляемого и управляемого модуля. Неуправляемый модуль — это библиотека DLL, которая определяет функцию, которая принимает массив целых чисел. Второй модуль — это управляемое приложение командной строки, которое импортирует эту функцию, но определяет ее в терминах управляемого массива и использует атрибут, <xref:System.Runtime.InteropServices.MarshalAsAttribute> чтобы указать, что массив должен быть преобразован в собственный массив при вызове.

Управляемый модуль компилируется с помощью/CLR.

```cpp
// TraditionalDll4.cpp
// compile with: /LD /EHsc
#include <iostream>

#define TRADITIONALDLL_EXPORTS
#ifdef TRADITIONALDLL_EXPORTS
#define TRADITIONALDLL_API __declspec(dllexport)
#else
#define TRADITIONALDLL_API __declspec(dllimport)
#endif

extern "C" {
   TRADITIONALDLL_API void TakesAnArray(int len, int[]);
}

void TakesAnArray(int len, int a[]) {
   printf_s("[unmanaged]\n");
   for (int i=0; i<len; i++)
      printf("%d = %d\n", i, a[i]);
}
```

```cpp
// MarshalBlitArray.cpp
// compile with: /clr
using namespace System;
using namespace System::Runtime::InteropServices;

value struct TraditionalDLL {
   [DllImport("TraditionalDLL4.dll")]
   static public void TakesAnArray(
   int len,[MarshalAs(UnmanagedType::LPArray)]array<int>^);
};

int main() {
   array<int>^ b = gcnew array<int>(3);
   b[0] = 11;
   b[1] = 33;
   b[2] = 55;
   TraditionalDLL::TakesAnArray(3, b);

   Console::WriteLine("[managed]");
   for (int i=0; i<3; i++)
      Console::WriteLine("{0} = {1}", i, b[i]);
}
```

Обратите внимание, что ни одна часть библиотеки DLL не предоставляется управляемому коду с помощью традиционной директивы #include. Фактически, поскольку библиотека DLL доступна только во время выполнения, проблемы с функциями, импортированными с помощью, <xref:System.Runtime.InteropServices.DllImportAttribute> не будут обнаружены во время компиляции.

## <a name="see-also"></a>См. также раздел

[Использование явного вызова PInvoke в C++ (атрибут DllImport)](../dotnet/using-explicit-pinvoke-in-cpp-dllimport-attribute.md)
