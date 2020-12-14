---
description: 'Дополнительные сведения: Отладка C++ страницы свойств'
title: Страницы свойств отладки C++
ms.date: 07/24/2019
ms.topic: article
ms.assetid: 78115a6b-3799-4515-814e-8566b5bdc55d
f1_keywords:
- VC.Project.IVCLocalDebugPageObject.Command
- VC.Project.IVCLocalDebugPageObject.CommandArguments
- VC.Project.IVCLocalDebugPageObject.WorkingDirectory
- VC.Project.IVCLocalDebugPageObject.Attach
- VC.Project.IVCLocalDebugPageObject.DebuggerType
- VC.Project.IVCLocalDebugPageObject.Environment
- VC.Project.IVCLocalDebugPageObject.GPUDebuggerTargetType
- VC.Project.IVCLocalDebugPageObject.GPUBreakOnAllThreads
- VC.Project.IVCLocalDebugPageObject.EnvironmentMerge
- VC.Project.IVCLocalDebugPageObject.SQLDebugging
- VC.Project.IVCLocalDebugPageObject.AmpDefaultAccelerator
- VC.Project.IVCRemoteDebugPageObject.RemoteCommand
- VC.Project.IVCRemoteDebugPageObject.CommandArguments
- VC.Project.IVCRemoteDebugPageObject.WorkingDirectory
- VC.Project.IVCRemoteDebugPageObject.RemoteMachine
- VC.Project.IVCRemoteDebugPageObject.Remote
- VC.Project.IVCRemoteDebugPageObject.DebuggerType
- VC.Project.IVCRemoteDebugPageObject.Environment
- VC.Project.IVCRemoteDebugPageObject.GPUDebuggerTargetType
- VC.Project.IVCRemoteDebugPageObject.GPUBreakOnAllThreads
- VC.Project.IVCRemoteDebugPageObject.Attach
- VC.Project.IVCRemoteDebugPageObject.SQLDebugging
- VC.Project.IVCRemoteDebugPageObject.DeploymentDirectory
- VC.Project.IVCRemoteDebugPageObject.AdditionalFiles
- VC.Project.IVCRemoteDebugPageObject.Remote
- VC.Project.IVCRemoteDebugPageObject.AmpDefaultAccelerator
- VC.Project.VCDebugSettings.WebBrowser.WebBrowserDebuggerHttpUrl
- VC.Project.VCDebugSettings.WebBrowser.DebuggerType
- VC.Project.IVCWebSvcDebugPageObject.HttpUrl
- VC.Project.IVCWebSvcDebugPageObject.DebuggerType
- VC.Project.IVCWebSvcDebugPageObject.SQLDebugging
ms.openlocfilehash: 16a7fec317485dd20a430baab9a413586f913fa3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201746"
---
# <a name="c-debugging-property-pages"></a>Страницы свойств отладки C++

Эти страницы свойств находятся в разделе   >  **Свойства** проекта свойства  >  **конфигурации**  >  **Отладка**. Выберите тип отладчика в раскрывающемся элементе управления. Дополнительные сведения об отладке кода C++ см. [в разделе Учебник. изучение отладки кода c++ с помощью Visual Studio](/visualstudio/debugger/getting-started-with-the-debugger-cpp) и [Отладка машинного кода](/visualstudio/debugger/debugging-native-code).

## <a name="local-windows-debugger-property-page"></a>Локальная страница свойств отладчика Windows

### <a name="command"></a>Команда

Команда отладки для выполнения.

### <a name="command-arguments"></a>Аргументы команды

Аргументы командной строки, передаваемые приложению.

### <a name="working-directory"></a>Рабочий каталог

Рабочий каталог приложения. По умолчанию каталог, содержащий файл проекта.

### <a name="attach"></a>Attach

Указывает, должен ли отладчик пытаться присоединиться к существующему процессу при запуске отладки.

### <a name="debugger-type"></a>Тип отладчика

Определение тип используемого отладчика. Если задано значение Авто, тип отладчика будет выбран на основе содержимого файла exe.

**Choices**

- **Только машинный код** — только машинный код
- Только **управляемый** — только управляемый
- **Смешанные**
- **Авто**
- **Скрипт-скрипт**
- **Только GPU (C++ amp)** — только gpu (C++ amp)

### <a name="environment"></a>Среда

Указывает окружение для отлаживаемой программы или переменные для слияния с существующей средой.

### <a name="debugging-accelerator-type"></a>Тип ускорителя отладки

Тип ускорителя отладки для использования при отладке кода GPU. (Доступно, если активен отладчик GPU).

### <a name="gpu-default-breakpoint-behavior"></a>Поведение по умолчанию для точки останова GPU

Задает частоту разрыва отладчика GPU.

**Choices**

- **Останов один раз для каждой** деформации
- **Прервать для каждого потока (например, поведение ЦП)** — прервать для каждого потока (например, поведение ЦП).

### <a name="merge-environment"></a>Объединить среду

Объединить указанные переменные среды с существующей средой.

### <a name="sql-debugging"></a>Отладка SQL

Присоедините отладчик SQL.

### <a name="amp-default-accelerator"></a>Ускоритель по умолчанию для AMP

Переопределить выбор ускорителя по умолчанию C++ AMP. Свойство не применяется при отладке управляемого кода.

## <a name="remote-windows-debugger-property-page"></a>Страница свойств удаленного отладчика Windows

Дополнительные сведения об удаленной отладке см. [в разделе Удаленная отладка Visual C++ проекта в Visual Studio](/visualstudio/debugger/remote-debugging-cpp).

### <a name="remote-command"></a>Удаленная команда

Команда отладки для выполнения.

### <a name="remote-command-arguments"></a>Аргументы удаленной команды

Аргументы командной строки, передаваемые приложению.

### <a name="working-directory"></a>Рабочий каталог

Рабочий каталог приложения. По умолчанию каталог, содержащий файл проекта.

### <a name="remote-server-name"></a>Имя удаленного сервера

Указывает имя удаленного сервера.

### <a name="connection"></a>Подключение

Указывает тип соединения.

**Choices**

- **Удаленный с проверкой** подлинности Windows — удаленный с [проверкой подлинности Windows](/windows-server/security/windows-authentication/windows-authentication-overview).
- **Удаленный без проверки подлинности** — удаленный без проверки подлинности.

### <a name="debugger-type"></a>Тип отладчика

Определение тип используемого отладчика. Если задано значение Авто, тип отладчика будет выбран на основе содержимого файла exe.

**Choices**

- **Только машинный код** — только машинный код
- Только **управляемый** — только управляемый
- **Смешанные**
- **Авто**
- **Скрипт-скрипт**
- **Только GPU (C++ amp)** — только gpu (C++ amp)

### <a name="environment"></a>Среда

Указывает окружение для отлаживаемой программы или переменные для слияния с существующей средой.

### <a name="debugging-accelerator-type"></a>Тип ускорителя отладки

Тип ускорителя отладки для использования при отладке кода GPU. (Доступно, если активен отладчик GPU).

### <a name="gpu-default-breakpoint-behavior"></a>Поведение по умолчанию для точки останова GPU

Задает частоту разрыва отладчика GPU.

**Choices**

- **Останов один раз для каждой** деформации
- **Прервать для каждого потока (например, поведение ЦП)** — прервать для каждого потока (например, поведение ЦП).

### <a name="attach"></a>Attach

Указывает, должен ли отладчик пытаться присоединиться к существующему процессу при запуске отладки.

### <a name="sql-debugging"></a>Отладка SQL

Присоедините отладчик SQL.

### <a name="deployment-directory"></a>Каталог развертывания

Если при отладке на удаленном компьютере необходимо скопировать содержимое выходных данных проекта (за исключением PDB-файлов) на удаленный компьютер, укажите здесь путь.

### <a name="additional-files-to-deploy"></a>Дополнительные файлы развертывания

При отладке на удаленном компьютере указанные здесь файлы и каталоги (помимо выходных данных проекта) копируются в каталог развертывания, если он указан.

### <a name="deploy-visual-c-debug-runtime-libraries"></a>Развертывание отладочных библиотек времени выполнения Visual C++

Указывает, следует ли развертывать отладочные библиотеки среды выполнения для активной платформы (Win32, x64 или ARM).

### <a name="amp-default-accelerator"></a>Ускоритель по умолчанию для AMP

Переопределить выбор ускорителя по умолчанию C++ AMP. Свойство не применяется при отладке управляемого кода.

## <a name="web-browser-debugger-property-page"></a>Страница свойств отладчика веб-браузера

### <a name="http-url"></a>URL-АДРЕС HTTP

Указывает URL-адрес для проекта.

### <a name="debugger-type"></a>Тип отладчика

Определение тип используемого отладчика. Если задано значение Авто, тип отладчика будет выбран на основе содержимого файла exe.

**Choices**

- **Только машинный код** — только машинный код
- Только **управляемый** — только управляемый
- **Смешанные**
- **Авто**
- **Скрипт-скрипт**

## <a name="web-service-debugger-property-page"></a>Страница свойств отладчика веб-службы

### <a name="http-url"></a>URL-АДРЕС HTTP

Указывает URL-адрес для проекта.

### <a name="debugger-type"></a>Тип отладчика

Определение тип используемого отладчика. Если задано значение Авто, тип отладчика будет выбран на основе содержимого файла exe.

**Choices**

- **Только машинный код** — только машинный код
- Только **управляемый** — только управляемый
- **Смешанные**
- **Авто**
- **Скрипт-скрипт**

### <a name="sql-debugging"></a>Отладка SQL

Присоедините отладчик SQL.
