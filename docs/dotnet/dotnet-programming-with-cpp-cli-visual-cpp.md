---
title: Программирование .NET с использованием C++/CLI
description: Узнайте, как использовать C++/CLI для создания приложений и компонентов .NET в Visual Studio.
ms.date: 12/08/2020
helpviewer_keywords:
- programming [C++], .NET programming
- .NET Framework [C++]
- .NET applications [C++]
- Visual C++, .NET programming
ms.openlocfilehash: 80a9743016976e307158608134155dc7272d44a8
ms.sourcegitcommit: 754df5278f795f661d4eeb0d4cacc908aa630159
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "96933187"
---
# <a name="net-programming-with-ccli"></a>Программирование .NET с использованием C++/CLI

::: moniker range="msvc-140"

По умолчанию проекты CLR, созданные с помощью Visual Studio 2015, предназначены для целевой платформы .NET Framework 4.5.2. Вы можете выбрать .NET Framework 4,6 при создании нового проекта. В диалоговом окне **Новый проект** измените целевую платформу в раскрывающемся списке в верхней части диалогового окна. Чтобы изменить целевую платформу для существующего проекта, закройте проект, измените файл проекта ( *`.vcxproj`* ) и измените значение целевой версии .NET Framework на 4,6. Изменения вступят в силу при следующем открытии проекта.

::: moniker-end
::: moniker range="msvc-150"

В Visual Studio 2017 целевой .NET Framework по умолчанию является 4.6.1. Селектор версии платформы находится в нижней части диалогового окна **Новый проект** .

## <a name="install-ccli-support-in-visual-studio-2017"></a>Установка поддержки C++/CLI в Visual Studio 2017

C++/CLI сам по себе не устанавливается по умолчанию при установке рабочей нагрузки Visual Studio C++. Чтобы установить компонент после установки Visual Studio, откройте Visual Studio Installer. Нажмите кнопку **изменить** рядом с установленной версией Visual Studio. Перейдите на вкладку **установленные компоненты** . Прокрутите вниз до раздела **компиляторы, средства сборки и среды выполнения** и выберите **Поддержка C++/CLI**. Выберите **изменить** , чтобы обновить Visual Studio.

::: moniker-end
::: moniker range="msvc-160"

В Visual Studio 2019 целевой платформой по умолчанию для проектов .NET Core является 5,0. Для проектов .NET Frameworks значение по умолчанию — 4.7.2. Средство выбора версии .NET Framework находится на странице **Настройка нового проекта** диалогового окна **Создание нового проекта** .
## <a name="install-ccli-support-in-visual-studio-2019"></a>Установка поддержки C++/CLI в Visual Studio 2019

C++/CLI сам по себе не устанавливается по умолчанию при установке рабочей нагрузки Visual Studio C++. Чтобы установить компонент после установки Visual Studio, откройте Visual Studio Installer. Нажмите кнопку **изменить** рядом с установленной версией Visual Studio. Перейдите на вкладку **установленные компоненты** . Прокрутите вниз до раздела **компиляторы, средства сборки и среды выполнения** и выберите последнюю **поддержку C++/CLI для компонента v142 Build Tools** . Выберите **изменить** , чтобы обновить Visual Studio.

::: moniker-end

## <a name="in-this-section"></a>В этом разделе

[Задачи C++/CLI](../dotnet/cpp-cli-tasks.md)

[Взаимодействие машинного кода и платформы.NET](../dotnet/native-and-dotnet-interoperability.md)

[Чистый и проверяемый код (C++/CLI)](../dotnet/pure-and-verifiable-code-cpp-cli.md)

[Регулярные выражения (C++/CLI)](../dotnet/regular-expressions-cpp-cli.md)

[Обработка файлов и ввод-вывод (C++/CLI)](../dotnet/file-handling-and-i-o-cpp-cli.md)

[Операции с графикой (C++/CLI)](../dotnet/graphics-operations-cpp-cli.md)

[Операции Windows (C++/CLI)](../dotnet/windows-operations-cpp-cli.md)

[Доступ к данным с помощью ADO.NET (C++/CLI)](../dotnet/data-access-using-adonet-cpp-cli.md)

[Взаимодействие с другими языками .NET (C++/CLI)](../dotnet/interoperability-with-other-dotnet-languages-cpp-cli.md)

[Сериализация (C++/CLI)](../dotnet/serialization-cpp-cli.md)

[Управляемые типы (C++/CLI)](../dotnet/managed-types-cpp-cli.md)

[Отражение (C++/CLI)](../dotnet/reflection-cpp-cli.md)

[Сборки со строгими именами (подписывание сборок) (C++/CLI)](../dotnet/strong-name-assemblies-assembly-signing-cpp-cli.md)

[Класс Debug (C++/CLI)](../dotnet/debug-class-cpp-cli.md)

[Справочник по библиотеке STL/CLR](../dotnet/stl-clr-library-reference.md)

[Библиотека поддержки C++](../dotnet/cpp-support-library.md)

[Исключения в C++/CLI](../dotnet/exceptions-in-cpp-cli.md)

[упаковка-преобразование (C++/CLI)](../dotnet/boxing-cpp-cli.md)

## <a name="see-also"></a>См. также раздел

[Взаимодействие машинного кода и платформы.NET](../dotnet/native-and-dotnet-interoperability.md)
