---
description: 'Дополнительные сведения: регулярные выражения (C++/CLI)'
title: Регулярные выражения (C++/CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- regular expressions [C++]
- .NET Framework [C++], regular expressions
- regular expressions [C++], about regular expressions
- parsing strings [C++]
- examples [C++], strings
- regular expressions [C++], parsing strings
- Split method, parsing strings
- strings [C++], parsing
- substrings, simple matches
- searching, exact substring matches
- strings [C++], exact substring matching
- regular expressions [C++], simple matching
- IsMatch method
- strings [C++], extracting data from
- formatted strings [C++]
- regular expressions [C++], extracting data fields
- data [C++], extracting from strings
- regular expressions [C++], rearranging data
- data [C++], rearranging
- search and replace
- Replace method
- regular expressions [C++], search and replace
- strings [C++], formatting
- data [C++], formatting
- regular expressions [C++], validating data formatting
ms.assetid: 838bab49-0dbc-4089-a604-ef146269ef5a
ms.openlocfilehash: 429a121ec7acad46437a344b089f5c6a1ce4243b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245815"
---
# <a name="regular-expressions-ccli"></a>Регулярные выражения (C++/CLI)

Демонстрирует различные операции со строками с использованием классов регулярных выражений в .NET Framework.

В следующих разделах демонстрируется использование <xref:System.Text.RegularExpressions> пространства имен .NET Framework (а в одном случае <xref:System.String.Split%2A?displayProperty=fullName> метода) для поиска, анализа и изменения строк.

## <a name="parse-strings-using-regular-expressions"></a><a name="parse_regex"></a> Анализ строк с помощью регулярных выражений

В следующем примере кода показан простой синтаксический анализ строк с помощью <xref:System.Text.RegularExpressions.Regex> класса в <xref:System.Text.RegularExpressions?displayProperty=fullName> пространстве имен. Создается строка, содержащая несколько типов разделений слов. Затем строка анализируется с помощью <xref:System.Text.RegularExpressions.Regex> класса в сочетании с <xref:System.Text.RegularExpressions.Match> классом. Затем каждое слово в предложении отображается отдельно.

### <a name="example"></a>Пример

```cpp
// regex_parse.cpp
// compile with: /clr
#using <system.dll>

using namespace System;
using namespace System::Text::RegularExpressions;

int main( )
{
   int words = 0;
   String^ pattern = "[a-zA-Z]*";
   Console::WriteLine( "pattern : '{0}'", pattern );
   Regex^ regex = gcnew Regex( pattern );

   String^ line = "one\ttwo three:four,five six  seven";
   Console::WriteLine( "text : '{0}'", line );
   for( Match^ match = regex->Match( line );
        match->Success; match = match->NextMatch( ) )
   {
      if( match->Value->Length > 0 )
      {
         words++;
         Console::WriteLine( "{0}", match->Value );
      }
   }
   Console::WriteLine( "Number of Words : {0}", words );

   return 0;
}
```

## <a name="parse-strings-using-the-split-method"></a><a name="parse_split"></a> Анализ строк с помощью метода Split

В следующем примере кода показано использование <xref:System.String.Split%2A?displayProperty=fullName> метода для извлечения каждого слова из строки. Строка, содержащая несколько типов разделений слов, создается и затем анализируется путем вызова <xref:System.String.Split%2A> со списком разделений. Затем каждое слово в предложении отображается отдельно.

### <a name="example"></a>Пример

```cpp
// regex_split.cpp
// compile with: /clr
using namespace System;

int main()
{
   String^ delimStr = " ,.:\t";
   Console::WriteLine( "delimiter : '{0}'", delimStr );
   array<Char>^ delimiter = delimStr->ToCharArray( );
   array<String^>^ words;
   String^ line = "one\ttwo three:four,five six seven";

   Console::WriteLine( "text : '{0}'", line );
   words = line->Split( delimiter );
   Console::WriteLine( "Number of Words : {0}", words->Length );
   for (int word=0; word<words->Length; word++)
      Console::WriteLine( "{0}", words[word] );

   return 0;
}
```

## <a name="use-regular-expressions-for-simple-matching"></a><a name="regex_simple"></a> Использование регулярных выражений для простого сопоставления

В следующем примере кода регулярные выражения используются для поиска точных совпадений подстрок. Поиск выполняется с помощью статического <xref:System.Text.RegularExpressions.Regex.IsMatch%2A> метода, который принимает в качестве входных данных две строки. Первая — строка для поиска, а вторая — шаблон для поиска.

### <a name="example"></a>Пример

```cpp
// regex_simple.cpp
// compile with: /clr
#using <System.dll>

using namespace System;
using namespace System::Text::RegularExpressions;

int main()
{
   array<String^>^ sentence =
   {
      "cow over the moon",
      "Betsy the Cow",
      "cowering in the corner",
      "no match here"
   };

   String^ matchStr = "cow";
   for (int i=0; i<sentence->Length; i++)
   {
      Console::Write( "{0,24}", sentence[i] );
      if ( Regex::IsMatch( sentence[i], matchStr,
                     RegexOptions::IgnoreCase ) )
         Console::WriteLine("  (match for '{0}' found)", matchStr);
      else
         Console::WriteLine("");
   }
   return 0;
}
```

## <a name="use-regular-expressions-to-extract-data-fields"></a><a name="regex_extract"></a> Использование регулярных выражений для извлечения полей данных

В следующем примере кода показано использование регулярных выражений для извлечения данных из форматированной строки. В следующем примере кода класс используется <xref:System.Text.RegularExpressions.Regex> для указания шаблона, соответствующего адресу электронной почты. Этот Паттер включает идентификаторы полей, которые можно использовать для извлечения частей имени пользователя и узла каждого адреса электронной почты. <xref:System.Text.RegularExpressions.Match>Класс используется для выполнения фактического сопоставления шаблонов. Если указан допустимый адрес электронной почты, имя пользователя и имена узлов извлекаются и отображаются.

### <a name="example"></a>Пример

```cpp
// Regex_extract.cpp
// compile with: /clr
#using <System.dll>

using namespace System;
using namespace System::Text::RegularExpressions;

int main()
{
    array<String^>^ address=
    {
        "jay@southridgevideo.com",
        "barry@adatum.com",
        "treyresearch.net",
        "karen@proseware.com"
    };

    Regex^ emailregex = gcnew Regex("(?<user>[^@]+)@(?<host>.+)");

    for (int i=0; i<address->Length; i++)
    {
        Match^ m = emailregex->Match( address[i] );
        Console::Write("\n{0,25}", address[i]);

        if ( m->Success )
        {
            Console::Write("   User='{0}'",
            m->Groups["user"]->Value);
            Console::Write("   Host='{0}'",
            m->Groups["host"]->Value);
        }
        else
            Console::Write("   (invalid email address)");
        }

    Console::WriteLine("");
    return 0;
}
```

## <a name="use-regular-expressions-to-rearrange-data"></a><a name="regex_rearrange"></a> Использование регулярных выражений для изменения порядка данных

В следующем примере кода показано, как можно использовать .NET Framework поддержки регулярных выражений для изменения порядка или переформатирования данных. В следующем примере кода <xref:System.Text.RegularExpressions.Regex> классы и используются <xref:System.Text.RegularExpressions.Match> для извлечения первых и последних имен из строки и последующего вывода этих элементов имени в обратном порядке.

<xref:System.Text.RegularExpressions.Regex>Класс используется для создания регулярного выражения, описывающего текущий формат данных. Предполагается, что два имени разделяются запятыми и могут использовать любой пробел вокруг запятой. <xref:System.Text.RegularExpressions.Match>Затем метод используется для анализа каждой строки. В случае успеха первые и последние имена извлекаются из <xref:System.Text.RegularExpressions.Match> объекта и отображаются.

### <a name="example"></a>Пример

```cpp
// regex_reorder.cpp
// compile with: /clr
#using <System.dll>
using namespace System;
using namespace Text::RegularExpressions;

int main()
{
   array<String^>^ name =
   {
      "Abolrous, Sam",
      "Berg,Matt",
      "Berry , Jo",
      "www.contoso.com"
   };

   Regex^ reg = gcnew Regex("(?<last>\\w*)\\s*,\\s*(?<first>\\w*)");

   for ( int i=0; i < name->Length; i++ )
   {
      Console::Write( "{0,-20}", name[i] );
      Match^ m = reg->Match( name[i] );
      if ( m->Success )
      {
         String^ first = m->Groups["first"]->Value;
         String^ last = m->Groups["last"]->Value;
         Console::WriteLine("{0} {1}", first, last);
      }
      else
         Console::WriteLine("(invalid)");
   }
   return 0;
}
```

## <a name="use-regular-expressions-to-search-and-replace"></a><a name="regex_search"></a> Использование регулярных выражений для поиска и замены

В следующем примере кода показано, как класс регулярного выражения <xref:System.Text.RegularExpressions.Regex> можно использовать для выполнения поиска и замены. Это делается с помощью <xref:System.Text.RegularExpressions.Regex.Replace%2A> метода. Используемая версия принимает в качестве входных данных две строки: изменяемую строку и строку, которая будет вставлена вместо разделов (если таковые имеются), соответствующих шаблону, заданному <xref:System.Text.RegularExpressions.Regex> объекту.

Этот код заменяет все цифры в строке символами подчеркивания (_), а затем заменяет их пустой строкой, фактически удаляя их. Тот же результат можно выполнить за один шаг, но в демонстрационных целях используются два шага.

### <a name="example"></a>Пример

```cpp
// regex_replace.cpp
// compile with: /clr
#using <System.dll>
using namespace System::Text::RegularExpressions;
using namespace System;

int main()
{
   String^ before = "The q43uick bro254wn f0ox ju4mped";
   Console::WriteLine("original  : {0}", before);

   Regex^ digitRegex = gcnew Regex("(?<digit>[0-9])");
   String^ after = digitRegex->Replace(before, "_");
   Console::WriteLine("1st regex : {0}", after);

   Regex^ underbarRegex = gcnew Regex("_");
   String^ after2 = underbarRegex->Replace(after, "");
   Console::WriteLine("2nd regex : {0}", after2);

   return 0;
}
```

## <a name="use-regular-expressions-to-validate-data-formatting"></a><a name="regex_validate"></a> Использование регулярных выражений для проверки форматирования данных

В следующем примере кода показано использование регулярных выражений для проверки форматирования строки. В следующем примере кода строка должна содержать допустимый номер телефона. В следующем примере кода используется строка "\d {3} -\d {3} -\d {4} " для указания того, что каждое поле представляет допустимый номер телефона. "D" в строке указывает цифру, а аргумент после каждого "d" указывает количество цифр, которое должно присутствовать. В этом случае число должно быть разделено дефисами.

### <a name="example"></a>Пример

```cpp
// regex_validate.cpp
// compile with: /clr
#using <System.dll>

using namespace System;
using namespace Text::RegularExpressions;

int main()
{
   array<String^>^ number =
   {
      "123-456-7890",
      "444-234-22450",
      "690-203-6578",
      "146-893-232",
      "146-839-2322",
      "4007-295-1111",
      "407-295-1111",
      "407-2-5555",
   };

   String^ regStr = "^\\d{3}-\\d{3}-\\d{4}$";

   for ( int i = 0; i < number->Length; i++ )
   {
      Console::Write( "{0,14}", number[i] );

      if ( Regex::IsMatch( number[i], regStr ) )
         Console::WriteLine(" - valid");
      else
         Console::WriteLine(" - invalid");
   }
   return 0;
}
```

## <a name="related-sections"></a>Связанные разделы

[Регулярные выражения в .NET Framework](/dotnet/standard/base-types/regular-expressions)

## <a name="see-also"></a>См. также раздел

[Программирование .NET с использованием C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)
