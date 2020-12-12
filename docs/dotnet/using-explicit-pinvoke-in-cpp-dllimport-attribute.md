---
description: 'Дополнительные сведения о: использование явного вызова PInvoke в C++ (атрибут DllImport)'
title: Использование явного вызова Pinvoke в C++ (атрибут DllImport)
ms.date: 11/04/2016
helpviewer_keywords:
- marshaling [C++], platform invoke
- C++ Interop, platform invoke
- interop [C++], platform invoke
- platform invoke [C++], marshaling in C++
- data marshaling [C++], platform invoke
ms.assetid: 18e5218c-6916-48a1-a127-f66e22ef15fc
ms.openlocfilehash: 6c49195cdb677474809435a5bd826808260680e7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97305483"
---
# <a name="using-explicit-pinvoke-in-c-dllimport-attribute"></a>Использование явного вызова Pinvoke в C++ (атрибут DllImport)

.NET Framework предоставляет явные функции вызова неуправляемого кода (или PInvoke) с `Dllimport` атрибутом, позволяя управляемым приложениям вызывать неуправляемые функции, Упакованные в библиотеки DLL. Явный вызов PInvoke необходим в ситуациях, когда неуправляемые API упакованы в виде библиотек DLL, а исходный код недоступен. Для вызова функций Win32, например, требуется PInvoke. В противном случае используйте неявный P {Invoke; см. Дополнительные сведения об [использовании взаимодействия C++ (неявный PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md) .

PInvoke работает с помощью <xref:System.Runtime.InteropServices.DllImportAttribute> . Этот атрибут, который принимает имя библиотеки DLL в качестве первого аргумента, помещается перед объявлением функции для каждой точки входа библиотеки DLL, которая будет использоваться. Сигнатура функции должна совпадать с именем функции, экспортируемой библиотекой DLL (Однако преобразование некоторых типов может быть выполнено неявно путем определения `DllImport` объявлений в терминах управляемых типов.)

Результатом является управляемая точка входа для каждой собственной функции DLL, которая содержит необходимый код перехода (или преобразователь) и простые преобразования данных. Затем управляемые функции могут вызывать библиотеку DLL через эти точки входа. Код, вставленный в модуль в результате вызова PInvoke, полностью управляется.

## <a name="in-this-section"></a>в этом разделе

- [Вызов собственных функций из управляемого кода](../dotnet/calling-native-functions-from-managed-code.md)

- [Инструкции. вызов собственных библиотек DLL из управляемого кода с помощью PInvoke](../dotnet/how-to-call-native-dlls-from-managed-code-using-pinvoke.md)

- [Инструкции. Маршалирование строк с помощью PInvoke](../dotnet/how-to-marshal-strings-using-pinvoke.md)

- [Инструкции. Маршалирование структур с помощью PInvoke](../dotnet/how-to-marshal-structures-using-pinvoke.md)

- [Инструкции. Маршалирование массивов с помощью PInvoke](../dotnet/how-to-marshal-arrays-using-pinvoke.md)

- [Инструкции. маршалирование указателей функций с помощью PInvoke](../dotnet/how-to-marshal-function-pointers-using-pinvoke.md)

- [Инструкции. маршалирование внедренных указателей с помощью PInvoke](../dotnet/how-to-marshal-embedded-pointers-using-pinvoke.md)

## <a name="see-also"></a>См. также раздел

[Вызов собственных функций из управляемого кода](../dotnet/calling-native-functions-from-managed-code.md)
