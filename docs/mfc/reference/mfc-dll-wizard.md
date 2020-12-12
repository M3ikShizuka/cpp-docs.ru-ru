---
description: 'Дополнительные сведения: мастер библиотек DLL MFC'
title: мастер DLL [MFC]
ms.date: 11/04/2016
f1_keywords:
- vc.appwiz.mfc.dll.overview
helpviewer_keywords:
- MFC DLLs [MFC], creating
- MFC DLL Wizard
- DLLs [MFC], MFC
- DLL wizard [MFC]
- MFC DLLs [MFC]
- DLLs [MFC], creating
ms.assetid: 4e936031-7e39-4f40-a295-42a09c5ff264
ms.openlocfilehash: 0f786255c22e644335c5154e0f14add59a2a418a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97219165"
---
# <a name="mfc-dll-wizard"></a>мастер DLL [MFC]

При использовании мастера библиотек DLL MFC для создания проекта библиотеки DLL MFC вы получаете работающее начальное приложение со встроенными функциями, которые при компиляции реализуют базовые функции [библиотеки DLL](../../build/dlls-in-visual-cpp.md). Программа MFC Starter содержит файлы исходного кода C++ (CPP), файлы ресурсов (RC) и файл проекта (VCXPROJ). Код, созданный в этих начальных файлах, основан на MFC. Дополнительные сведения см. в сведениях о файлах в Readme.txt, которые создаются для проекта в Visual Studio, а также о [классах и функциях, созданных мастером MFC DLL](../../mfc/reference/classes-and-functions-generated-by-the-mfc-dll-wizard.md) .

## <a name="overview"></a>Общие сведения

На этой странице мастера описываются текущие [Параметры приложения для создаваемого проекта DLL MFC](../../mfc/reference/application-settings-mfc-dll-wizard.md) . По умолчанию проект создается как обычный проект DLL MFC (MFC Shared) без дополнительных параметров.

Чтобы изменить эти значения по умолчанию, щелкните **Параметры приложения** в левом столбце мастера и внесите изменения на этой странице мастера DLL MFC.

После создания проекта MFC DLL можно добавить в проект объекты или элементы управления с помощью [мастеров Visual C++ кода](../../ide/adding-functionality-with-code-wizards-cpp.md).

В базовый проект MFC DLL можно выполнять следующие задачи и типы улучшений.

- [Экспорт из библиотеки DLL](../../build/exporting-from-a-dll.md)

- [Связывание исполняемого файла с библиотекой DLL](../../build/linking-an-executable-to-a-dll.md)

- [Инициализация библиотеки DLL](../../build/run-time-library-behavior.md#initializing-a-dll)

## <a name="see-also"></a>См. также

[Проекты Visual Studio — C++](../../build/creating-and-managing-visual-cpp-projects.md)<br/>
[Страницы свойств](../../build/reference/property-pages-visual-cpp.md)<br/>
[Настройка компилятора и свойств сборки](../../build/working-with-project-properties.md)<br/>
[Класс MFC](../../mfc/reference/adding-an-mfc-class.md)<br/>
[Добавление функции-члена](../../ide/adding-a-member-function-visual-cpp.md)<br/>
[Реализация интерфейса](../../ide/implementing-an-interface-visual-cpp.md)<br/>
