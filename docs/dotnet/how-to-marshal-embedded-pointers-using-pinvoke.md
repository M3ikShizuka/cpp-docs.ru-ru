---
description: Дополнительные сведения см. в статье как маршалировать внедренные указатели с помощью PInvoke.
title: Практическое руководство. Маршалинг внедренных указателей с помощью PInvoke
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- embedded pointers [C++]
- interop [C++], embedded pointers
- platform invoke [C++], embedded pointers
- marshaling [C++], embedded pointers
- data marshaling [C++], embedded pointers
ms.assetid: f12c1b9a-4f82-45f8-83c8-3fc9321dbb98
ms.openlocfilehash: d31660a9a8ba345b380d442bb4484e332fe9d7cd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97302560"
---
# <a name="how-to-marshal-embedded-pointers-using-pinvoke"></a>Практическое руководство. Маршалинг внедренных указателей с помощью PInvoke

Функции, реализованные в неуправляемых библиотеках DLL, могут вызываться из управляемого кода с помощью функции вызова неуправляемой платформы (P/Invoke). Если исходный код библиотеки DLL недоступен, вызов P/Invoke является единственным вариантом взаимодействия. Однако, в отличие от других языков .NET, Visual C++ предоставляет альтернативу P/Invoke. Дополнительные сведения см. в статьях [использование взаимодействия c++ (неявный PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md) и [инструкции: маршалирование внедренных указателей с помощью взаимодействия c++](../dotnet/how-to-marshal-embedded-pointers-using-cpp-interop.md).

## <a name="example"></a>Пример

Передача структур в машинный код требует создания управляемой структуры, которая эквивалентна структуре данных в машинном виде. Однако для структур, содержащих указатели, требуется специальная обработка. Для каждого внедренного указателя в собственной структуре управляемая версия структуры должна содержать экземпляр <xref:System.IntPtr> типа. Кроме того, память для этих экземпляров должна быть явно выделена, инициализирована и освобождена с помощью <xref:System.Runtime.InteropServices.Marshal.AllocCoTaskMem%2A> <xref:System.Runtime.InteropServices.Marshal.StructureToPtr%2A> методов, и <xref:System.Runtime.InteropServices.Marshal.FreeCoTaskMem%2A> .

Следующий код состоит из неуправляемого и управляемого модуля. Неуправляемый модуль — это библиотека DLL, которая определяет функцию, которая принимает структуру с именем Листстринг, содержащую указатель, и функцию с именем Такеслистструкт. Управляемый модуль — это приложение командной строки, которое импортирует функцию Такеслистструкт и определяет структуру с именем Млистструкт, эквивалентную собственной Листструкт, за исключением того, что Double * представлен с <xref:System.IntPtr> экземпляром. Перед вызовом Такеслистструкт функция Main выделяет и инициализирует память, на которую ссылается это поле.

```cpp
// TraditionalDll6.cpp
// compile with: /EHsc /LD
#include <stdio.h>
#include <iostream>
#define TRADITIONALDLL_EXPORTS
#ifdef TRADITIONALDLL_EXPORTS
#define TRADITIONALDLL_API __declspec(dllexport)
#else
#define TRADITIONALDLL_API __declspec(dllimport)
#endif

#pragma pack(push, 8)
struct ListStruct {
   int count;
   double* item;
};
#pragma pack(pop)

extern "C" {
   TRADITIONALDLL_API void TakesListStruct(ListStruct);
}

void TakesListStruct(ListStruct list) {
   printf_s("[unmanaged] count = %d\n", list.count);
   for (int i=0; i<list.count; i++)
      printf_s("array[%d] = %f\n", i, list.item[i]);
}
```

```cpp
// EmbeddedPointerMarshalling.cpp
// compile with: /clr
using namespace System;
using namespace System::Runtime::InteropServices;

[StructLayout(LayoutKind::Sequential, Pack=8)]
value struct MListStruct {
   int count;
   IntPtr item;
};

value struct TraditionalDLL {
    [DllImport("TraditionalDLL6.dll")]
   static public void TakesListStruct(MListStruct);
};

int main() {
   array<double>^ parray = gcnew array<double>(10);
   Console::WriteLine("[managed] count = {0}", parray->Length);

   Random^ r = gcnew Random();
   for (int i=0; i<parray->Length; i++) {
      parray[i] = r->NextDouble() * 100.0;
      Console::WriteLine("array[{0}] = {1}", i, parray[i]);
   }

   int size = Marshal::SizeOf(double::typeid);
   MListStruct list;
   list.count = parray->Length;
   list.item = Marshal::AllocCoTaskMem(size * parray->Length);

   for (int i=0; i<parray->Length; i++) {
      IntPtr t = IntPtr(list.item.ToInt32() + i * size);
      Marshal::StructureToPtr(parray[i], t, false);
   }

   TraditionalDLL::TakesListStruct( list );
   Marshal::FreeCoTaskMem(list.item);
}
```

Обратите внимание, что ни одна часть библиотеки DLL не предоставляется управляемому коду с помощью традиционной директивы #include. На самом деле библиотека DLL доступна только во время выполнения, поэтому проблемы с функциями, импортированными с помощью, <xref:System.Runtime.InteropServices.DllImportAttribute> не будут обнаружены во время компиляции.

## <a name="see-also"></a>См. также раздел

[Использование явного вызова PInvoke в C++ (атрибут DllImport)](../dotnet/using-explicit-pinvoke-in-cpp-dllimport-attribute.md)
