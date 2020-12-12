---
description: Дополнительные сведения о развертывании собственных классических приложений (Visual C++)
title: Развертывание классических приложений неуправляемого кода (Visual C++)
ms.date: 05/11/2018
helpviewer_keywords:
- deploying applications [C++]
- application deployment [C++]
- Visual C++, application deployment
- application deployment [C++], about application deployment
- deploying applications [C++], about deploying applications
- distributing applications [C++]
ms.assetid: 37f1691e-d67c-41e4-926e-528a237a9bac
ms.topic: overview
ms.openlocfilehash: c3da460266eb630e7ac243f523fa6e89a79fa1f0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329448"
---
# <a name="deploying-native-desktop-applications-visual-c"></a>Развертывание классических приложений неуправляемого кода (Visual C++)

Развертывание — это процесс, с помощью которого готовое приложение или компонент распространяются для установки на других компьютерах. Планирование развертывания начинается при создании приложения на компьютере разработчика. Развертывание завершается, когда приложение установлено и готово для запуска на компьютере пользователя.

Visual Studio предоставляет различные технологии развертывания приложений Windows. К ним относятся развертывание ClickOnce и развертывание установщика Windows.

- ClickOnce можно использовать для развертывания приложений C++, предназначенных для среды CLR, — смешанных, полностью управляемых и проверяемых сборок. Хотя установщик Windows можно использовать для развертывания управляемого приложения, рекомендуется использовать компонент ClickOnce, так как он позволяет воспользоваться функциями безопасности .NET Framework, например подписыванием манифеста. ClickOnce не поддерживает развертывание собственных приложений C++. Дополнительные сведения см. в разделе [ClickOnce Deployment for Visual C++ Applications](clickonce-deployment-for-visual-cpp-applications.md).

- Установщик Windows можно использовать для развертывания приложений C++ неуправляемого кода или приложений C++, предназначенных для среды CLR.

В статьях в этом разделе документации рассматриваются следующие вопросы: как проверить работу приложения Visual C++ неуправляемого кода на любом компьютере, предоставляющем поддерживаемую целевую платформу, файлы, которые необходимо включить в пакет установки, и рекомендуемые способы распространения компонентов, от которых зависит работа приложения.

## <a name="in-this-section"></a>в этом разделе

- [Развертывание в Visual C++](deployment-in-visual-cpp.md)

- [Концепции развертывания](deployment-concepts.md)

- [Основные сведения о зависимостях приложения Visual C++](understanding-the-dependencies-of-a-visual-cpp-application.md)

- [Определение библиотек DLL для распространения](determining-which-dlls-to-redistribute.md)

- [Выбор метода развертывания](choosing-a-deployment-method.md)

- [Развертывание универсальной CRT](universal-crt-deployment.md).

- [Распространение файлов Visual C++](redistributing-visual-cpp-files.md)

- [Примеры развертывания](deployment-examples.md)

- [Распространение клиентских веб-приложений](redistributing-web-client-applications.md)

- [Развертывание ClickOnce для приложений Visual C++](clickonce-deployment-for-visual-cpp-applications.md)

- [Выполнение приложения C++ с параметром /clr в более ранней версии среды выполнения](running-a-cpp-clr-application-on-a-previous-runtime-version.md)

## <a name="related-sections"></a>Связанные разделы

- [Создание изолированных приложений и параллельных сборок C/C++](../build/building-c-cpp-isolated-applications-and-side-by-side-assemblies.md)

- [Развертывание](/dotnet/framework/deployment/index)

- [Устранение неполадок в изолированных приложениях и параллельных сборках на C/C++](../build/troubleshooting-c-cpp-isolated-applications-and-side-by-side-assemblies.md)
