---
description: 'Дополнительные сведения о: основные понятия панели инструментов'
title: Основные сведения о панелях инструментов
ms.date: 11/04/2016
f1_keywords:
- RT_TOOLBAR
helpviewer_keywords:
- embedding toolbar in frame window class [MFC]
- application wizards [MFC], installing default application toolbars
- toolbars [MFC], creating
- resources [MFC], toolbar
- toolbar controls [MFC], toolbars created using Application Wizard
- toolbar controls [MFC], command ID
- RT_TOOLBAR resource [MFC]
- toolbars [MFC], adding default using Application Wizard
- LoadBitmap method [MFC], toolbars
- Toolbar editor [MFC], Application Wizard
- command IDs [MFC], toolbar buttons
- SetButtons method [MFC]
- CToolBar class [MFC], default toolbars in Application Wizard
- frame window classes [MFC], toolbar embedded in
- LoadToolBar method [MFC]
ms.assetid: cc00aaff-8a56-433b-b0c0-b857d76b4ffd
ms.openlocfilehash: ed52c5878482f2ff0fa1c31a133fd2948d21a76e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264392"
---
# <a name="toolbar-fundamentals"></a>Основные сведения о панелях инструментов

В этой статье описывается основная реализация MFC, которая позволяет добавить в приложение Панель инструментов по умолчанию, выбрав параметр в мастере приложений. Здесь рассматриваются такие темы:

- [Параметр панели инструментов мастера приложений](#_core_the_appwizard_toolbar_option)

- [Панель инструментов в коде](#_core_the_toolbar_in_code)

- [Изменение ресурса панели инструментов](#_core_editing_the_toolbar_resource)

- [Несколько панелей инструментов](#_core_multiple_toolbars)

## <a name="the-application-wizard-toolbar-option"></a><a name="_core_the_appwizard_toolbar_option"></a> Параметр панели инструментов мастера приложений

Чтобы получить одну панель инструментов с кнопками по умолчанию, выберите стандартный параметр закрепляемая панель инструментов на странице функции интерфейса пользователя. В приложение добавляется код, который:

- Создает объект панели инструментов.

- Управляет панелью инструментов, включая ее возможность закреплять или перемещать.

## <a name="the-toolbar-in-code"></a><a name="_core_the_toolbar_in_code"></a> Панель инструментов в коде

Панель инструментов — это объект [CToolBar](../mfc/reference/ctoolbar-class.md) , объявленный как элемент данных `CMainFrame` класса приложения. Иными словами, объект панели инструментов внедряется в основной объект окна фрейма. Это означает, что MFC создает панель инструментов при создании окна фрейма и уничтожает панель инструментов при удалении окна фрейма. В следующем объявлении разделяемого класса для приложения с многодокументным интерфейсом (MDI) отображаются элементы данных для встроенной панели инструментов и встроенной строки состояния. Он также показывает переопределение `OnCreate` функции члена.

[!code-cpp[NVC_MFCListView#6](../atl/reference/codesnippet/cpp/toolbar-fundamentals_1.h)]

Создание панели инструментов происходит в `CMainFrame::OnCreate` . MFC вызывает метод [OnCreate](../mfc/reference/cwnd-class.md#oncreate) после создания окна для рамки, но перед тем, как оно станет видимым. По умолчанию `OnCreate` Мастер приложений создает следующие задачи панели инструментов:

1. Вызывает `CToolBar` функцию элемента [CREATE](../mfc/reference/ctoolbar-class.md#create) объекта, чтобы создать базовый объект [CToolBarCtrl](../mfc/reference/ctoolbarctrl-class.md) .

1. Вызывает [лоадтулбар](../mfc/reference/ctoolbar-class.md#loadtoolbar) для загрузки сведений о ресурсе панели инструментов.

1. Вызывает функции для включения закрепления, плавающего и всплывающих подсказок. Дополнительные сведения об этих вызовах см. в статье [закрепление и плавающие панели инструментов](../mfc/docking-and-floating-toolbars.md).

> [!NOTE]
> В общем примере MFC [докктул](../overview/visual-cpp-samples.md) содержатся иллюстрации старых и новых панелей инструментов MFC. Панели инструментов, использующие, `COldToolbar` должны вызываться на шаге 2 в `LoadBitmap` (а не `LoadToolBar` ) и в `SetButtons` . Для новых панелей инструментов требуются вызовы `LoadToolBar` .

Вызовы закрепления, плавающего и всплывающих подсказок являются необязательными. При желании вы можете удалить эти строки `OnCreate` . Результатом является панель инструментов, которая остается фиксированной, не может быть плавающей или переброской и не может отображать подсказки.

## <a name="editing-the-toolbar-resource"></a><a name="_core_editing_the_toolbar_resource"></a> Изменение ресурса панели инструментов

Панель инструментов по умолчанию, которая появляется в мастере приложений, основана на **RT_TOOLBAR** настраиваемом ресурсе, представленном в MFC версии 4,0. Этот ресурс можно изменить с помощью [редактора панелей инструментов](../windows/toolbar-editor.md). Редактор позволяет легко добавлять, удалять и изменять порядок кнопок. Он содержит графический редактор для кнопок, которые очень похожи на общие графические редакторы в Visual C++. Если вы редактировали панели инструментов в предыдущих версиях Visual C++, задача будет гораздо проще.

Чтобы подключить кнопку панели инструментов к команде, присвойте кнопке идентификатор команды, например `ID_MYCOMMAND` . Укажите идентификатор команды на странице свойств кнопки в редакторе панели инструментов. Затем создайте функцию обработчика для команды (Дополнительные сведения см. [в разделе Сопоставление сообщений с функциями](../mfc/reference/mapping-messages-to-functions.md) ).

Новые функции члена [CToolBar](../mfc/reference/ctoolbar-class.md) работают с ресурсом **RT_TOOLBAR** . [Лоадтулбар](../mfc/reference/ctoolbar-class.md#loadtoolbar) теперь занимает место [лоадбитмап](../mfc/reference/ctoolbar-class.md#loadbitmap) , чтобы загрузить растровое изображение для кнопок панели инструментов, и [сетбуттонс](../mfc/reference/ctoolbar-class.md#setbuttons) , чтобы установить стили кнопок и соединить кнопки с растровыми изображениями.

Дополнительные сведения об использовании редактора панелей инструментов см. в разделе [Редактор панелей инструментов](../windows/toolbar-editor.md).

## <a name="multiple-toolbars"></a><a name="_core_multiple_toolbars"></a> Несколько панелей инструментов

Мастер приложений предоставляет одну панель инструментов по умолчанию. Если в приложении требуется больше одной панели инструментов, можно смоделировать код для дополнительных панелей инструментов на основе кода, созданного мастером, для панели инструментов по умолчанию.

Если вы хотите отобразить панель инструментов в качестве результата выполнения команды, необходимо выполнить следующие действия.

- Создайте новый ресурс панели инструментов с помощью редактора панелей инструментов и загрузите его `OnCreate` с помощью функции-члена [лоадтулбар](../mfc/reference/ctoolbar-class.md#loadtoolbar) .

- Внедрите новый объект [CToolBar](../mfc/reference/ctoolbar-class.md) в главный класс окна фрейма.

- Выполните вызовы функций в `OnCreate` для закрепления или переброски панели инструментов, установки ее стилей и т. д.

### <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Реализация панели инструментов MFC (Общие сведения о панелях инструментов)](../mfc/mfc-toolbar-implementation.md)

- [Закрепленные и плавающие панели инструментов](../mfc/docking-and-floating-toolbars.md)

- [Всплывающие подсказки панели инструментов](../mfc/toolbar-tool-tips.md)

- Классы [CToolBar](../mfc/reference/ctoolbar-class.md) и [CToolBarCtrl](../mfc/reference/ctoolbarctrl-class.md)

- [Использование элемента управления "Панель инструментов"](../mfc/working-with-the-toolbar-control.md)

- [Использование старых панелей инструментов](../mfc/using-your-old-toolbars.md)

## <a name="see-also"></a>См. также раздел

[Реализация панели инструментов MFC](../mfc/mfc-toolbar-implementation.md)
