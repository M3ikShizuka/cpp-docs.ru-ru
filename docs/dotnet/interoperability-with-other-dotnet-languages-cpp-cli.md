---
description: 'Дополнительные сведения: взаимодействие с другими языками .NET (C++/CLI)'
title: Совместимость с другими языками .NET (C++/CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- C++, indexers
- indexers, consuming C#
- as C# keyword [C++]
- is C# keyword [C++]
- lock statement
- lock C# keyword [C++]
ms.assetid: a5902cf8-a14d-4559-aefb-c178615d45bb
ms.openlocfilehash: 51cead7fcc7dedc05f0225facf10fe70a3d606fd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316613"
---
# <a name="interoperability-with-other-net-languages-ccli"></a>Совместимость с другими языками .NET (C++/CLI)

В подразделах этого раздела показано, как создавать сборки в Visual C++, которые используют или предоставляют функциональные возможности для сборок, написанных на C# или Visual Basic.

## <a name="consume-a-c-indexer"></a><a name="consume_indexer"></a> Использование индексатора C#

Visual C++ не содержит индексаторов; Он имеет индексированные свойства. Чтобы использовать индексатор C#, необходимо получить доступ к индексатору так, как если бы он был индексированным свойством.

Дополнительные сведения об индексаторах см. в следующих статьях:

- [Индексаторы](/dotnet/csharp/programming-guide/indexers/index)

### <a name="example"></a>Пример

В следующей программе C# определяется индексатор.

```csharp
// consume_cs_indexers.cs
// compile with: /target:library
using System;
public class IndexerClass {
   private int [] myArray = new int[100];
   public int this [int index] {   // Indexer declaration
      get {
         // Check the index limits.
         if (index < 0 || index >= 100)
            return 0;
         else
            return myArray[index];
      }
      set {
         if (!(index < 0 || index >= 100))
            myArray[index] = value;
      }
   }
}
/*
// code to consume the indexer
public class MainClass {
   public static void Main() {
      IndexerClass b = new IndexerClass();

      // Call indexer to initialize elements 3 and 5
      b[3] = 256;
      b[5] = 1024;
      for (int i = 0 ; i <= 10 ; i++)
         Console.WriteLine("Element #{0} = {1}", i, b[i]);
   }
}
*/
```

### <a name="example"></a>Пример

Эта Visual C++ программа использует индексатор.

```cpp
// consume_cs_indexers_2.cpp
// compile with: /clr
#using "consume_cs_indexers.dll"
using namespace System;

int main() {
   IndexerClass ^ ic = gcnew IndexerClass;
   ic->default[0] = 21;
   for (int i = 0 ; i <= 10 ; i++)
      Console::WriteLine("Element #{0} = {1}", i, ic->default[i]);
}
```

```Output
Element #0 = 21
Element #1 = 0
Element #2 = 0
Element #3 = 0
Element #4 = 0
Element #5 = 0
Element #6 = 0
Element #7 = 0
Element #8 = 0
Element #9 = 0
Element #10 = 0
```

## <a name="implement-is-and-as-c-keywords"></a><a name="implement_isas"></a> Реализуйте ключевое слово и как ключевые слова C#

В этом разделе показано, как реализовать функциональные возможности `is` `as` ключевых слов и C# в Visual C++.

### <a name="example"></a>Пример

```cpp
// CS_is_as.cpp
// compile with: /clr
using namespace System;

interface class I {
public:
   void F();
};

ref struct C : public I {
   virtual void F( void ) { }
};

template < class T, class U >
Boolean isinst(U u) {
   return dynamic_cast< T >(u) != nullptr;
}

int main() {
   C ^ c = gcnew C();
   I ^ i = safe_cast< I ^ >(c);   // is (maps to castclass in IL)
   I ^ ii = dynamic_cast< I ^ >(c);   // as (maps to isinst in IL)

   // simulate 'as':
   Object ^ o = "f";
   if ( isinst< String ^ >(o) )
      Console::WriteLine("o is a string");
}
```

```Output
o is a string
```

## <a name="implement-the-lock-c-keyword"></a><a name="implement_locak"></a> Реализация ключевого слова C# lock

В этом разделе показано, как реализовать `lock` ключевое слово C# в Visual C++.

Также можно использовать `lock` класс в библиотеке поддержки C++. Дополнительные сведения см. в разделе [Синхронизация (класс Lock)](../dotnet/synchronization-lock-class.md) .

### <a name="example"></a>Пример

```cpp
// CS_lock_in_CPP.cpp
// compile with: /clr
using namespace System::Threading;
ref class Lock {
   Object^ m_pObject;
public:
   Lock( Object ^ pObject ) : m_pObject( pObject ) {
      Monitor::Enter( m_pObject );
   }
   ~Lock() {
      Monitor::Exit( m_pObject );
   }
};

ref struct LockHelper {
   void DoSomething();
};

void LockHelper::DoSomething() {
   // Note: Reference type with stack allocation semantics to provide
   // deterministic finalization

   Lock lock( this );
   // LockHelper instance is locked
}

int main()
{
   LockHelper lockHelper;
   lockHelper.DoSomething();
   return 0;
}
```

## <a name="see-also"></a>См. также раздел

[Программирование .NET с использованием C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)
