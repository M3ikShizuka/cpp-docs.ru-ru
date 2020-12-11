---
description: Дополнительные сведения о мастере проектов ATL
title: Мастер проектов ATL
ms.date: 11/04/2016
f1_keywords:
- vc.appwiz.atl.com.overview
helpviewer_keywords:
- ATL projects, creating
- ATL Project Wizard
ms.assetid: 564d2aaf-5b8e-4c2a-a925-ca40a283ea34
ms.openlocfilehash: a254447d0590abd3d68090dac04c3b6134f94b19
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158677"
---
# <a name="atl-project-wizard"></a>Мастер проектов ATL

Библиотека активных шаблонов (ATL) — это набор классов C++ на основе шаблона, упрощающих написание небольших и быстрых COM-объектов. Мастер проектов ATL создает проект со структурами, содержащими COM-объекты.

## <a name="overview"></a>Общие сведения

На этой странице мастера описываются текущие [Параметры приложения для создаваемого проекта ATL](../../atl/reference/application-settings-atl-project-wizard.md) . По умолчанию проект имеет следующие параметры.

- Библиотека динамической компоновки указывает, что сервер является библиотекой DLL и, следовательно, внутрипроцессный сервер.

- С атрибутами указывает, что в проекте используются атрибуты.

Чтобы изменить эти значения по умолчанию, щелкните **Параметры приложения** в левом столбце мастера и внесите изменения на этой странице мастера проектов ATL.

Сведения о параметрах проекта по умолчанию, включая выбор кодировки и связывание значений по умолчанию, см. в разделе [конфигурации проектов ATL по умолчанию](../../atl/reference/default-atl-project-configurations.md).

После создания проекта ATL можно добавить в проект объекты или элементы управления с помощью [мастеров Visual C++ кода](../../ide/adding-functionality-with-code-wizards-cpp.md). С помощью мастеров кода можно внести в базовый проект ATL следующие типы улучшений:

- [Добавление объектов и элементов управления в проект ATL](../../atl/reference/adding-objects-and-controls-to-an-atl-project.md)

- [Добавление нового интерфейса в проект ATL](../../atl/reference/adding-a-new-interface-in-an-atl-project.md)

- [Добавление компонента COM+ 1,0 в проект ATL](../../atl/reference/adding-an-atl-com-plus-1-0-component.md)

Кроме того, при создании и усовершенствовании проекта ATL следует учитывать следующие задачи.

- [Отключение возможности создания объекта ATL](../../atl/reference/making-an-atl-object-noncreatable.md)

- [Оптимизация компилятора для проекта ATL](../../atl/reference/specifying-compiler-optimization-for-an-atl-project.md)

Можно указать свойства проекта (например, [связать статически с CRT](../../atl/programming-with-atl-and-c-run-time-code.md)) на странице [свойств проекта](../../build/reference/general-property-page-project.md) , а также задать [конфигурации сборки](/visualstudio/ide/understanding-build-configurations) для проекта ATL.

## <a name="see-also"></a>См. также

[Проекты Visual Studio — C++](../../build/creating-and-managing-visual-cpp-projects.md)<br/>
[Типы проектов C++ в Visual Studio](../../build/reference/visual-cpp-project-types.md)<br/>
[Основы COM-объектов ATL](../../atl/fundamentals-of-atl-com-objects.md)<br/>
[Программирование с помощью ATL и кода Run-Time C](../../atl/programming-with-atl-and-c-run-time-code.md)<br/>
[Руководство](../../atl/active-template-library-atl-tutorial.md)
