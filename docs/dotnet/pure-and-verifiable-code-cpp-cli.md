---
description: 'Дополнительные сведения: чистый и проверяемый код (C++/CLI)'
title: Чистый и проверяемый код (C++/CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- /clr compiler option [C++], verifiable assemblies
- /clr compiler option [C++], mixed assemblies
- pure MSIL [C++]
- verifiable assemblies [C++]
- verifiably type-safe code [C++]
- /clr compiler option [C++], pure assemblies
- .NET Framework [C++], pure and verifiable code
- assemblies [C++], mixed code
- verifiable assemblies [C++], about verifiable assemblies
- mixed assemblies [C++], about mixed assemblies
- pure MSIL [C++], about pure code
- assemblies [C++], verifiable code
- mixed assemblies [C++]
- assemblies [C++], pure code
ms.assetid: 9050e110-fa11-4356-b56c-665187ff871c
ms.openlocfilehash: 64224f7f462b5e11e522648a5b64ec9d568dc53f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97276768"
---
# <a name="pure-and-verifiable-code-ccli"></a>Чистый и проверяемый код (C++/CLI)

Для программирования .NET Visual C++ в Visual Studio 2017 поддерживает создание смешанных сборок с помощью параметра компилятора [/CLR (компиляция среды CLR)](../build/reference/clr-common-language-runtime-compilation.md) . Параметры **/clr: pure** и **clr: безопасный** являются устаревшими в Visual Studio 2015 и не поддерживаются в Visual Studio 2017. Если ваш код должен быть надежным или проверяемым, рекомендуется перенести его на C#.

## <a name="mixed-clr"></a>Mixed (/CLR)

Смешанные сборки (скомпилированные с **/CLR**) содержат как неуправляемые, так и управляемые части, что позволяет им использовать функции .NET, но по-прежнему содержать машинный код. Это позволяет обновлять приложения и компоненты для использования функций .NET без необходимости переписывать весь проект. Использование Visual C++ для смешивания управляемого и машинного кода таким образом называется взаимодействием C++. Дополнительные сведения см. в разделе [смешанные (собственные и управляемые) сборки](../dotnet/mixed-native-and-managed-assemblies.md) и [взаимодействие машинного и .NET](../dotnet/native-and-dotnet-interoperability.md).

Вызовы, выполненные из управляемых сборок в собственные библиотеки DLL с помощью P/Invoke, будут компилироваться, но могут завершиться ошибкой во время выполнения в зависимости от настроек безопасности.

Существует один сценарий создания кода, который будет передавать компилятор, но это приведет к непроверяемой сборке: вызов виртуальной функции через экземпляр объекта с помощью оператора разрешения области.  Например, так: `MyObj -> A::VirtualFunction();`.

## <a name="see-also"></a>См. также раздел

- [Программирование .NET с использованием C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)
