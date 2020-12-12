---
description: Дополнительные сведения о взаимодействии машин и .NET
title: Взаимодействие исходного кода и платформы.NET
ms.date: 11/04/2016
helpviewer_keywords:
- interop [C++]
- .NET Framework [C++], interoperability with Visual C++
- interoperability [C++], about .NET interoperability
- interop [C++], about .NET interoperability
- managed code [C++], interoperability
- native code [C++]
- interoperability [C++]
- MFC [C++], .NET integration
- unmanaged code interoperability [C++]
- Visual C++, interoperability
- native code [C++], .NET interoperatibility
ms.assetid: f3ec6c99-c745-4256-b95b-f1d12ba17a5a
ms.openlocfilehash: 0276c4401b56f453549cf31433cc6f558daf1c02
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97255643"
---
# <a name="native-and-net-interoperability"></a>Взаимодействие исходного кода и платформы.NET

Visual C++ поддерживает функции взаимодействия, которые позволяют управляемым и неуправляемым конструкциям совместно существовать и взаимодействовать в одной сборке и даже в одном файле. Небольшое подмножество этих функций, например P/Invoke, поддерживается и другими языками .NET, но большая часть поддержки взаимодействия, предоставляемая Visual C++, недоступна на других языках.

## <a name="in-this-section"></a>в этом разделе

[Смешанные (собственные и управляемые) сборки](../dotnet/mixed-native-and-managed-assemblies.md)<br/>
Описывает сборки, созданные с помощью параметра компилятора [/CLR (компиляция среды CLR)](../build/reference/clr-common-language-runtime-compilation.md) , который содержит как управляемые, так и неуправляемые функции.

[Использование пользовательского элемента управления формы Windows Forms в MFC](../dotnet/using-a-windows-form-user-control-in-mfc.md)<br/>
Описывает, как использовать классы поддержки MFC Windows Forms для размещения элементов управления Windows Forms в приложениях MFC.

[Вызов собственных функций из управляемого кода](../dotnet/calling-native-functions-from-managed-code.md)<br/>
Описывает, как можно использовать библиотеки DLL, отличные от CLR, в приложениях .NET.
