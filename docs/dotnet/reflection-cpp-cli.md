---
description: 'Дополнительные сведения: отражение (C++/CLI)'
title: Отражение (C++/CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- typeid keyword [C++]
- reflection [C++}, about reflection
- metadata, reflection
- GetType method
- .NET Framework [C++], reflection
- data types [C++], reflection
- reflection [C++}
- plug-ins [C++]
- reflection [C++}, plug-ins
- assemblies [C++], enumerating data types in
- public types [C++]
- reflection [C++], external assemblies
- assemblies [C++]
- data types [C++], enumerating
- public members [C++]
ms.assetid: 46b6ff4a-e441-4022-8892-78e69422f230
ms.openlocfilehash: a3a9a33a239ec678279455ea41b7c60749cc0189
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245802"
---
# <a name="reflection-ccli"></a>Отражение (C++/CLI)

Отражение позволяет проверять известные типы данных во время выполнения. Отражение допускает перечисление типов данных в заданной сборке, а также возможность обнаружения членов данного класса или типа значения. Это справедливо независимо от того, был ли тип известен или на него имеется ссылка во время компиляции. Это делает отражение полезным компонентом для средств разработки и управления кодом.

Обратите внимание, что указанное имя сборки является строгим именем (см. раздел [Создание и использование сборок Strong-Named](/dotnet/framework/app-domains/create-and-use-strong-named-assemblies)), включая версию сборки, язык и региональные параметры и сведения о подписывании. Обратите внимание, что можно получить имя пространства имен, в котором определяется тип данных, а также имя базового класса.

Самым распространенным способом доступа к функциям отражения является <xref:System.Object.GetType%2A> метод. Этот метод предоставляется <xref:System.Object?displayProperty=nameWithType> , из которого создаются все классы, собираемые сборщиком мусора.

> [!NOTE]
> Отражение EXE-файла, созданного с помощью компилятора Microsoft C++, допускается только в том случае, если исполняемый файл создан с помощью параметров компилятора **/clr: pure** или **/clr: Сейф** . Параметры компилятора **/clr: pure** и **/clr: Сейф** являются устаревшими в Visual Studio 2015 и недоступны в Visual Studio 2017. Дополнительные сведения см. в разделе [/CLR (компиляция CLR)](../build/reference/clr-common-language-runtime-compilation.md) .

Дополнительные сведения см. в разделе <xref:System.Reflection>.

## <a name="example-gettype"></a>Пример: GetType

`GetType`Метод возвращает указатель на <xref:System.Type> объект класса, который описывает тип в момент, когда он основан на объекте. (Объект **Type** не содержит сведений, относящихся к конкретному экземпляру.) Одним из таких элементов является полное имя типа, которое можно отобразить следующим образом:

Обратите внимание, что имя типа включает полную область, в которой определен тип, включая пространство имен и отображается в синтаксисе .NET с точкой в качестве оператора разрешения области.

```cpp
// vcpp_reflection.cpp
// compile with: /clr
using namespace System;
int main() {
   String ^ s = "sample string";
   Console::WriteLine("full type name of '{0}' is '{1}'", s, s->GetType());
}
```

```Output
full type name of 'sample string' is 'System.String'
```

## <a name="example-boxed-value-types"></a>Пример: типы упакованных значений

Типы значений также можно использовать с `GetType` функцией, но они должны быть упакованы первыми.

```cpp
// vcpp_reflection_2.cpp
// compile with: /clr
using namespace System;
int main() {
   Int32 i = 100;
   Object ^ o = i;
   Console::WriteLine("type of i = '{0}'", o->GetType());
}
```

```Output
type of i = 'System.Int32'
```

## <a name="example-typeid"></a>Пример: typeid

Как и в `GetType` случае с методом, оператор [typeid](../extensions/typeid-cpp-component-extensions.md) возвращает указатель на объект **типа** , поэтому этот код указывает имя типа **System. Int32**. Отображение имен типов является самой простой функцией отражения, но потенциально более полезной является проверка или обнаружение допустимых значений для перечислимых типов. Это можно сделать с помощью функции static **enum::** GetText, которая возвращает массив строк, каждый из которых содержит значение перечисления в текстовом виде.  Следующий пример извлекает массив строк, описывающих значения перечисления значений для перечисления **Options** (CLR), и отображает их в цикле.

Если в перечисление **Options** добавляется четвертый параметр, этот код сообщит о новом параметре без повторной компиляции, даже если перечисление определено в отдельной сборке.

```cpp
// vcpp_reflection_3.cpp
// compile with: /clr
using namespace System;

enum class Options {   // not a native enum
   Option1, Option2, Option3
};

int main() {
   array<String^>^ names = Enum::GetNames(Options::typeid);

   Console::WriteLine("there are {0} options in enum '{1}'",
               names->Length, Options::typeid);

   for (int i = 0 ; i < names->Length ; i++)
      Console::WriteLine("{0}: {1}", i, names[i]);

   Options o = Options::Option2;
   Console::WriteLine("value of 'o' is {0}", o);
}
```

```Output
there are 3 options in enum 'Options'
0: Option1
1: Option2
2: Option3
value of 'o' is Option2
```

## <a name="example-gettype-members-and-properties"></a>Пример: элементы и свойства GetType

`GetType`Объект поддерживает ряд элементов и свойств, которые можно использовать для проверки типа. Этот код извлекает и отображает некоторые из этих сведений:

```cpp
// vcpp_reflection_4.cpp
// compile with: /clr
using namespace System;
int main() {
   Console::WriteLine("type information for 'String':");
   Type ^ t = String::typeid;

   String ^ assemblyName = t->Assembly->FullName;
   Console::WriteLine("assembly name: {0}", assemblyName);

   String ^ nameSpace = t->Namespace;
   Console::WriteLine("namespace: {0}", nameSpace);

   String ^ baseType = t->BaseType->FullName;
   Console::WriteLine("base type: {0}", baseType);

   bool isArray = t->IsArray;
   Console::WriteLine("is array: {0}", isArray);

   bool isClass = t->IsClass;
   Console::WriteLine("is class: {0}", isClass);
}
```

```Output
type information for 'String':
assembly name: mscorlib, Version=1.0.5000.0, Culture=neutral,
PublicKeyToken=b77a5c561934e089
namespace: System
base type: System.Object
is array: False
is class: True
```

## <a name="example-enumeration-of-types"></a>Пример. Перечисление типов

Отражение также позволяет перечислить типы в сборке и элементы в классах. Чтобы продемонстрировать эту функцию, определите простой класс:

```cpp
// vcpp_reflection_5.cpp
// compile with: /clr /LD
using namespace System;
public ref class TestClass {
   int m_i;
public:
   TestClass() {}
   void SimpleTestMember1() {}
   String ^ SimpleMember2(String ^ s) { return s; }
   int TestMember(int i) { return i; }
   property int Member {
      int get() { return m_i; }
      void set(int i) { m_i = i; }
   }
};
```

## <a name="example-inspection-of-assemblies"></a>Пример. Проверка сборок

Если приведенный выше код компилируется в библиотеку DLL с именем vcpp_reflection_6.dll, можно использовать отражение для проверки содержимого этой сборки. Это включает использование функции API статического отражения XREF: System. Reflection. Assembly. Load% 2A? displayProperty = nameWithType для загрузки сборки. Эта функция возвращает адрес объекта **сборки** , который затем можно запросить о модулях и типах в.

После успешной загрузки сборки системой отражения массив объектов **типа** извлекается с помощью <xref:System.Reflection.Assembly.GetTypes%2A?displayProperty=nameWithType> функции. Каждый элемент массива содержит сведения о другом типе, хотя в данном случае определен только один класс. С помощью цикла каждый **тип** в этом массиве запрашивается о членах типа с помощью функции **Type::-Members** . Эта функция возвращает массив объектов **MethodInfo** , каждый объект которого содержит сведения о функции элемента, элементе данных или свойстве в типе.

Обратите внимание, что список методов включает функции, явно определенные в **TestClass** , и функции, неявно наследуемые от класса **System:: Object** . Как часть описания в .NET, а не в синтаксисе Visual C++, свойства отображаются как базовый элемент данных, к которому обращается функция Get/Set. Функции Get/Set в этом списке отображаются как обычные методы. Отражение поддерживается в среде CLR, а не компиляторе Microsoft C++.

Хотя этот код использовался для проверки сборки, которую вы определили, этот код можно также использовать для проверки сборок .NET. Например, если изменить TestAssembly на mscorlib, вы увидите список всех типов и методов, определенных в mscorlib.dll.

```cpp
// vcpp_reflection_6.cpp
// compile with: /clr
using namespace System;
using namespace System::IO;
using namespace System::Reflection;
int main() {
   Assembly ^ a = nullptr;
   try {
      // load assembly -- do not use file extension
      // will look for .dll extension first
      // then .exe with the filename
      a = Assembly::Load("vcpp_reflection_5");
   }
   catch (FileNotFoundException ^ e) {
      Console::WriteLine(e->Message);
      return -1;
   }

   Console::WriteLine("assembly info:");
   Console::WriteLine(a->FullName);
   array<Type^>^ typeArray = a->GetTypes();

   Console::WriteLine("type info ({0} types):", typeArray->Length);

   int totalTypes = 0;
   int totalMembers = 0;
   for (int i = 0 ; i < typeArray->Length ; i++) {
      // retrieve array of member descriptions
      array<MemberInfo^>^ member = typeArray[i]->GetMembers();

      Console::WriteLine("  members of {0} ({1} members):",
      typeArray[i]->FullName, member->Length);
      for (int j = 0 ; j < member->Length ; j++) {
         Console::Write("       ({0})",
         member[j]->MemberType.ToString() );
         Console::Write("{0}  ", member[j]);
         Console::WriteLine("");
         totalMembers++;
      }
      totalTypes++;
   }
   Console::WriteLine("{0} total types, {1} total members",
   totalTypes, totalMembers);
}
```

## <a name="how-to-implement-a-plug-in-component-architecture-using-reflection"></a><a name="implement"></a> Инструкции. Реализация Plug-In архитектуры компонентов с помощью отражения

В следующих примерах кода демонстрируется использование отражения для реализации простой "подключаемой" архитектуры. Первым списком является приложение, а вторым — подключаемый модуль. Приложение — это форма документа, которая заполняется с помощью любых классов на основе форм, находящихся в библиотеке DLL подключаемого модуля, предоставляемой в виде аргумента командной строки.

Приложение пытается загрузить предоставленную сборку с помощью <xref:System.Reflection.Assembly.Load%2A?displayProperty=fullName> метода. В случае успеха типы внутри сборки перечисляются с помощью <xref:System.Reflection.Assembly.GetTypes%2A?displayProperty=fullName> метода. Затем каждый тип проверяется на совместимость с помощью <xref:System.Type.IsAssignableFrom%2A?displayProperty=fullName> метода. В этом примере классы, найденные в предоставленной сборке, должны быть производными от класса, чтобы быть в <xref:System.Windows.Forms.Form> качестве подключаемого модуля.

После этого создаются экземпляры совместимых классов с помощью <xref:System.Activator.CreateInstance%2A?displayProperty=fullName> метода, который принимает в <xref:System.Type> качестве аргумента и возвращает указатель на новый экземпляр. Затем каждый новый экземпляр присоединяется к форме и отображается.

Обратите внимание, что <xref:System.Reflection.Assembly.Load%2A> метод не принимает имена сборок, включающих расширение файла. Функция Main в приложении обрезает все предоставленные расширения, поэтому следующий пример кода работает в любом случае.

### <a name="example"></a>Пример

Следующий код определяет приложение, которое принимает подключаемые модули. В качестве первого аргумента должно быть указано имя сборки. Эта сборка должна содержать по крайней мере один открытый <xref:System.Windows.Forms.Form> производный тип.

```cpp
// plugin_application.cpp
// compile with: /clr /c
#using <system.dll>
#using <system.drawing.dll>
#using <system.windows.forms.dll>

using namespace System;
using namespace System::Windows::Forms;
using namespace System::Reflection;

ref class PluggableForm : public Form  {
public:
   PluggableForm() {}
   PluggableForm(Assembly^ plugAssembly) {
      Text = "plug-in example";
      Size = Drawing::Size(400, 400);
      IsMdiContainer = true;

      array<Type^>^ types = plugAssembly->GetTypes( );
      Type^ formType = Form::typeid;

      for (int i = 0 ; i < types->Length ; i++) {
         if (formType->IsAssignableFrom(types[i])) {
            // Create an instance given the type description.
            Form^ f = dynamic_cast<Form^> (Activator::CreateInstance(types[i]));
            if (f) {
               f->Text = types[i]->ToString();
               f->MdiParent = this;
               f->Show();
            }
         }
      }
   }
};

int main() {
   Assembly^ a = Assembly::LoadFrom("plugin_application.exe");
   Application::Run(gcnew PluggableForm(a));
}
```

### <a name="example"></a>Пример

Следующий код определяет три класса, производных от <xref:System.Windows.Forms.Form> . Когда имя полученного имени сборки передается в исполняемый файл в предыдущем списке, каждый из этих трех классов будет обнаружен и создан, несмотря на тот факт, что они все неизвестны для ведущего приложения во время компиляции.

```cpp
// plugin_assembly.cpp
// compile with: /clr /LD
#using <system.dll>
#using <system.drawing.dll>
#using <system.windows.forms.dll>

using namespace System;
using namespace System::Windows::Forms;
using namespace System::Reflection;
using namespace System::Drawing;

public ref class BlueForm : public Form {
public:
   BlueForm() {
      BackColor = Color::Blue;
   }
};

public ref class CircleForm : public Form {
protected:
   virtual void OnPaint(PaintEventArgs^ args) override {
      args->Graphics->FillEllipse(Brushes::Green, ClientRectangle);
   }
};

public ref class StarburstForm : public Form {
public:
   StarburstForm(){
      BackColor = Color::Black;
   }
protected:
   virtual void OnPaint(PaintEventArgs^ args) override {
      Pen^ p = gcnew Pen(Color::Red, 2);
      Random^ r = gcnew Random( );
      Int32 w = ClientSize.Width;
      Int32 h = ClientSize.Height;
      for (int i=0; i<100; i++) {
         float x1 = w / 2;
         float y1 = h / 2;
         float x2 = r->Next(w);
         float y2 = r->Next(h);
         args->Graphics->DrawLine(p, x1, y1, x2, y2);
      }
   }
};
```

## <a name="how-to-enumerate-data-types-in-assemblies-using-reflection"></a><a name="enumerate"></a> Инструкции. Перечисление типов данных в сборках с помощью отражения

В следующем коде показано перечисление открытых типов и членов с помощью <xref:System.Reflection> .

При наличии имени сборки либо в локальном каталоге, либо в глобальном кэше сборок приведенный ниже код пытается открыть сборку и получить описания. В случае успеха каждый тип отображается с его открытыми членами.

Обратите внимание, что для этого <xref:System.Reflection.Assembly.Load%2A?displayProperty=fullName> не требуется расширение файла. Поэтому использование "mscorlib.dll" в качестве аргумента командной строки завершится ошибкой, при использовании только "mscorlib" приведет к отображению типов .NET Framework. Если имя сборки не указано, код обнаружит и сообщит о типах в текущей сборке (EXE-файл, полученном из этого кода).

### <a name="example"></a>Пример

```cpp
// self_reflection.cpp
// compile with: /clr
using namespace System;
using namespace System::Reflection;
using namespace System::Collections;

public ref class ExampleType {
public:
   ExampleType() {}
   void Func() {}
};

int main() {
   String^ delimStr = " ";
   array<Char>^ delimiter = delimStr->ToCharArray( );
   array<String^>^ args = Environment::CommandLine->Split( delimiter );

// replace "self_reflection.exe" with an assembly from either the local
// directory or the GAC
   Assembly^ a = Assembly::LoadFrom("self_reflection.exe");
   Console::WriteLine(a);

   int count = 0;
   array<Type^>^ types = a->GetTypes();
   IEnumerator^ typeIter = types->GetEnumerator();

   while ( typeIter->MoveNext() ) {
      Type^ t = dynamic_cast<Type^>(typeIter->Current);
      Console::WriteLine("   {0}", t->ToString());

      array<MemberInfo^>^ members = t->GetMembers();
      IEnumerator^ memberIter = members->GetEnumerator();
      while ( memberIter->MoveNext() ) {
         MemberInfo^ mi = dynamic_cast<MemberInfo^>(memberIter->Current);
         Console::Write("      {0}", mi->ToString( ) );
         if (mi->MemberType == MemberTypes::Constructor)
            Console::Write("   (constructor)");

         Console::WriteLine();
      }
      count++;
   }
   Console::WriteLine("{0} types found", count);
}
```

## <a name="see-also"></a>См. также раздел

- [Программирование .NET с использованием C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)
