---
description: 'Дополнительные сведения: мастер элементов управления ActiveX MFC'
title: мастер элементов управления MFC ActiveX
ms.date: 09/12/2018
f1_keywords:
- vc.appwiz.mfc.ctl.overview
helpviewer_keywords:
- ActiveX controls [MFC], MFC
- MFC ActiveX controls [MFC], wizards
- OLE controls [MFC], creating
- MFC ActiveX Control Wizard
- OLE controls [MFC]
ms.assetid: f19d698c-bdc3-4c74-af97-3d6ccb441b75
ms.openlocfilehash: f313f2a218c06a20eddbfff33e936109e4be2cf0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97219269"
---
# <a name="mfc-activex-control-wizard"></a>мастер элементов управления MFC ActiveX

Элемент управления ActiveX — это конкретный тип [сервера автоматизации](../../mfc/automation-servers.md); Это многократно используемый компонент. Приложение, в котором размещается элемент управления ActiveX, является [клиентом автоматизации](../../mfc/automation-clients.md) этого элемента управления. Если ваша цель состоит в создании такого многократно используемого компонента, используйте этот мастер для создания элемента управления. Дополнительные сведения см. в разделе [элементы управления ActiveX в MFC](../../mfc/mfc-activex-controls.md) .

>[!IMPORTANT]
> ActiveX — это устаревшая технология, которую не следует использовать для новой разработки. Дополнительные сведения о современных технологиях, которые заменяют ActiveX, см. в разделе [элементы управления ActiveX](../activex-controls.md).

Кроме того, можно создать приложение MFC сервера автоматизации с помощью [мастера приложений MFC](../../mfc/reference/mfc-application-wizard.md).

Элемент управления ActiveX, созданный с помощью этого мастера, может иметь пользовательский интерфейс, или он может быть невидимым. Этот параметр можно указать на странице [параметров управления](../../mfc/reference/control-settings-mfc-activex-control-wizard.md) в мастере. Элемент управления Timer — это пример элемента управления ActiveX, который должен быть невидимым.

Элементы управления ActiveX могут иметь сложный пользовательский интерфейс. Некоторые элементы управления могут быть подобны инкапсулированным формам: один элемент управления, содержащий множество полей, каждый элемент управления Windows в своем собственном правом. Например, объект автофрагментов, реализованный как элемент управления ActiveX MFC, может представлять пользовательский интерфейс, похожий на форму, с помощью которого пользователи могут считывать и изменять номер части, имя части и другие сведения. Дополнительные сведения см. в разделе [элементы управления ActiveX в MFC](../../mfc/mfc-activex-controls.md) .

Если необходимо создать контейнер для объектов ActiveX, см. раздел [Создание контейнера элементов управления ActiveX](../../mfc/reference/creating-an-mfc-activex-control-container.md).

Программа MFC Starter содержит файлы исходного кода C++ (CPP), файлы ресурсов (RC) и файл проекта (VCXPROJ). Код, созданный в этих начальных файлах, основан на MFC.

В следующем примере перечислены задачи и типы усовершенствований элемента управления ActiveX.

- [Оптимизация элемента управления ActiveX](../../mfc/mfc-activex-controls-optimization.md)

- [Добавление событий акции в элемент управления ActiveX](../../mfc/mfc-activex-controls-adding-stock-events-to-an-activex-control.md)

- [Добавление пользовательских событий](../../mfc/mfc-activex-controls-adding-custom-events.md)

- [Добавление методов хранения запасов](../../mfc/mfc-activex-controls-adding-stock-methods.md)

- [Добавление пользовательских методов](../../mfc/mfc-activex-controls-adding-custom-methods.md)

- [Добавление свойств запасов](../../mfc/mfc-activex-controls-adding-stock-properties.md)

- [Добавление пользовательских свойств](../../mfc/mfc-activex-controls-adding-custom-properties.md)

- [Программирование элементов управления ActiveX в контейнере элементов управления ActiveX](../../mfc/programming-activex-controls-in-a-activex-control-container.md)

## <a name="overview"></a>Общие сведения

На этой странице мастера описываются текущие параметры приложения для создаваемого проекта элемента управления ActiveX MFC. По умолчанию мастер создает проект следующим образом:

- Проект по умолчанию не создает лицензии или файлы справки во время выполнения. Эти параметры по умолчанию можно изменить на странице [Параметры приложения](../../mfc/reference/application-settings-mfc-activex-control-wizard.md) . На странице " **Обзор** " отображаются только те параметры, которые вы вносите на этой странице мастера элементов управления ActiveX.

- Проект включает класс элемента управления и класс страницы свойств на основе имени проекта. Имена проекта и имен файлов можно изменить на странице [имена элементов управления](../../mfc/reference/control-names-mfc-activex-control-wizard.md) .

- Элемент управления основан не на существующем элементе управления Windows, активируется, когда он становится видимым, имеет пользовательский интерфейс и включает диалоговое окно " **о программе** ". Эти параметры по умолчанию можно изменить на странице [Параметры управления](../../mfc/reference/control-settings-mfc-activex-control-wizard.md) .

## <a name="see-also"></a>См. также

[Проекты Visual Studio — C++](../../build/creating-and-managing-visual-cpp-projects.md)<br/>
[Типы проектов C++ в Visual Studio](../../build/reference/visual-cpp-project-types.md)<br/>
[Основные понятия](../../atl/active-template-library-atl-concepts.md)
