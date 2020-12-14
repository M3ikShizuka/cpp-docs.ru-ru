---
description: Дополнительные сведения о мастере приложений MFC
title: мастер приложений MFC
ms.date: 11/04/2016
f1_keywords:
- vc.appwiz.mfc.exe.overview
helpviewer_keywords:
- MFC Application Wizard
- executable files, creating
ms.assetid: 227ac090-921d-4b2f-be0a-66a5f4cab0d4
ms.openlocfilehash: 645f0e1ed3f1f35c109d524a8c63fa36231bc61a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97219217"
---
# <a name="mfc-application-wizard"></a>мастер приложений MFC

Мастер приложений MFC создает приложение, которое при компиляции реализует базовые функции исполняемого приложения Windows (exe). Приложение MFC Starter содержит файлы исходного кода C++ (CPP), файлы ресурсов (. RC), файлы заголовков (h) и файл проекта (VCXPROJ). Код, создаваемый в этих начальных файлах, основан на MFC.

> [!NOTE]
> В зависимости от выбранных параметров мастер создает дополнительные файлы в проекте. Например, при выборе **контекстной справки** на странице [Дополнительные компоненты](../../mfc/reference/advanced-features-mfc-application-wizard.md) мастер создает файлы, необходимые для компиляции файлов справки проекта. Дополнительные сведения о файлах, создаваемых мастером, см. в разделе [типы файлов, создаваемые для проектов Visual Studio C++](../../build/reference/file-types-created-for-visual-cpp-projects.md), а также в файле Readme.txt в проекте.

## <a name="overview"></a>Общие сведения

На этой странице мастера описываются текущие параметры приложения для создаваемого приложения MFC. По умолчанию мастер создает проект следующим образом:

- [Тип приложения, мастер приложений MFC](../../mfc/reference/application-type-mfc-application-wizard.md)

  - Проект создается с поддержкой многодокументного интерфейса с вкладками (MDI). Дополнительные сведения см. в разделе [SDI и MDI](../../mfc/sdi-and-mdi.md).

  - Проект использует [архитектуру "документ-представление](../../mfc/document-view-architecture.md)".

  - Проект использует библиотеки Юникода.

  - Проект создается с помощью стиля проекта Visual Studio и включает переключение визуального стиля.

  - Проект использует MFC в общей библиотеке DLL. Дополнительные сведения см. [в статье Создание библиотек DLL C/C++ в Visual Studio](../../build/dlls-in-visual-cpp.md).

- [Поддержка составных документов, мастер приложений MFC](../../mfc/reference/compound-document-support-mfc-application-wizard.md)

  - Проект не предоставляет поддержку для составных документов.

- [Строки шаблонов документов, мастер приложений MFC](../../mfc/reference/document-template-strings-mfc-application-wizard.md)

  - Проект использует имя проекта для строк шаблона документа по умолчанию.

- [Поддержка баз данных, мастер приложений MFC](../../mfc/reference/database-support-mfc-application-wizard.md)

  - Проект не обеспечивает поддержку баз данных.

- [Функции пользовательского интерфейса, мастер приложений MFC](../../mfc/reference/user-interface-features-mfc-application-wizard.md)

  - Проект реализует стандартные функции пользовательского интерфейса Windows, такие как системное меню, строка состояния, поля развертывания и сворачивания, поле **About** , стандартная строка меню и закрепляемая панель инструментов, а также дочерние фреймы.

- [Дополнительные функции, мастер приложений MFC](../../mfc/reference/advanced-features-mfc-application-wizard.md)

  - Проект поддерживает печать и предварительный просмотр печати.

  - Проект поддерживает элементы управления ActiveX. Дополнительные сведения см. в разделе [последовательность операций для создания элементов управления ActiveX](../../mfc/sequence-of-operations-for-creating-activex-controls.md).

  - Проект не поддерживает [автоматизацию](../../mfc/automation.md), [MAPI](../../mfc/mapi-support-in-mfc.md), [сокеты Windows](../../mfc/windows-sockets-in-mfc.md)или Active Accessibility.

  - Проект поддерживает закрепляемую панель **обозревателя** , панель закрепления **вывода** и **Свойства** панель закрепления.

- [Созданные классы, мастер приложений MFC](../../mfc/reference/generated-classes-mfc-application-wizard.md)

  - Класс представления проекта является производным от [класса CView](../../mfc/reference/cview-class.md).

  - Класс приложения проекта является производным от [класса CWinAppEx](../../mfc/reference/cwinappex-class.md).

  - Класс документа проекта является производным от [класса CDocument](../../mfc/reference/cdocument-class.md).

  - Класс основного фрейма проекта является производным от [класса CMDIFrameWndEx](../../mfc/reference/cmdiframewndex-class.md).

  - Класс дочернего фрейма проекта является производным от [класса CMDIChildWndEx](../../mfc/reference/cmdichildwndex-class.md).

Чтобы изменить эти параметры по умолчанию, щелкните соответствующий заголовок вкладки в левом столбце мастера и внесите изменения на появившейся странице.

После создания проекта приложения MFC в него можно добавлять объекты или элементы управления с помощью [мастеров Visual C++ кода](../../ide/adding-functionality-with-code-wizards-cpp.md).

## <a name="see-also"></a>См. также раздел

[Создание приложения MFC](../../mfc/reference/creating-an-mfc-application.md)<br/>
[Классические приложения MFC](../../mfc/mfc-desktop-applications.md)<br/>
[Использование классов для написания приложений для Windows](../../mfc/using-the-classes-to-write-applications-for-windows.md)
