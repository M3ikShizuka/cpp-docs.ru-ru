---
description: 'Дополнительные сведения о классе: Debug (C++/CLI)'
title: Класс Debug (C++/CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- Trace class, Visual C++
- .NET Framework [C++], Debug class
- Debug class
ms.assetid: 076bd528-1b6f-4e8a-a372-eb5849cf969a
ms.openlocfilehash: 255fe306684928faf836cd550005eea820d64ce5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97258438"
---
# <a name="debug-class-ccli"></a>Класс Debug (C++/CLI)

При использовании <xref:System.Diagnostics.Debug> в Visual C++ном приложении поведение не меняется между отладочной и окончательной сборками.

## <a name="remarks"></a>Комментарии

Поведение для аналогично <xref:System.Diagnostics.Trace> поведению для класса Debug, но зависит от определяемой трассировки символов. Это означает, что `#ifdef` для предотвращения отладки в сборке выпуска необходимо иметь любой код, связанный с трассировкой.

## <a name="example-always-executes-output-statements"></a>Пример: всегда выполняет выходные операторы

### <a name="description"></a>Описание

Следующий пример всегда выполняет выходные инструкции, независимо от того, выполняется ли компиляция с помощью **/ддебуг** или **/дтраце**.

### <a name="code"></a>Код

```cpp
// mcpp_debug_class.cpp
// compile with: /clr
#using <system.dll>
using namespace System::Diagnostics;
using namespace System;

int main() {
   Trace::Listeners->Add( gcnew TextWriterTraceListener( Console::Out ) );
   Trace::AutoFlush = true;
   Trace::Indent();
   Trace::WriteLine( "Entering Main" );
   Console::WriteLine( "Hello World." );
   Trace::WriteLine( "Exiting Main" );
   Trace::Unindent();

   Debug::WriteLine("test");
}
```

### <a name="output"></a>Выходные данные

```Output
    Entering Main
Hello World.
    Exiting Main
test
```

## <a name="example-use-ifdef-and-endif-directives"></a>Пример. Использование директив #ifdef и #endif

### <a name="description"></a>Описание

Чтобы получить ожидаемое поведение (т. е. не выводится тестовый вывод для сборки выпуска), необходимо использовать `#ifdef` `#endif` директивы и. Предыдущий пример кода изменяется ниже, чтобы продемонстрировать это исправление:

### <a name="code"></a>Код

```cpp
// mcpp_debug_class2.cpp
// compile with: /clr
#using <system.dll>
using namespace System::Diagnostics;
using namespace System;

int main() {
   Trace::Listeners->Add( gcnew TextWriterTraceListener( Console::Out ) );
   Trace::AutoFlush = true;
   Trace::Indent();

#ifdef TRACE   // checks for a debug build
   Trace::WriteLine( "Entering Main" );
   Console::WriteLine( "Hello World." );
   Trace::WriteLine( "Exiting Main" );
#endif
   Trace::Unindent();

#ifdef DEBUG   // checks for a debug build
   Debug::WriteLine("test");
#endif   //ends the conditional block
}
```

## <a name="see-also"></a>См. также

[Программирование .NET с использованием C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)
