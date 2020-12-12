---
description: 'Дополнительные сведения о: Справочник по MSBuild для проектов C++'
title: Справочник по MSBuild для проектов C++ в Visual Studio
ms.date: 12/08/2018
helpviewer_keywords:
- MSBuild reference [C++]
ms.openlocfilehash: 898757c8b7f1427c36e68a7227ec145abab8d078
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190618"
---
# <a name="msbuild-reference-for-c-projects"></a>Проекты С++. Справочник по MSBuild

MSBuild — это собственная система сборки для всех проектов в Visual Studio, включая проекты C++. При построении проекта в интегрированной среде разработки (IDE) Visual Studio он вызывает средство msbuild.exe, которое, в свою очередь, использует файл проекта VCXPROJ и различные файлы targets и PROPS. Как правило, мы настоятельно рекомендуем использовать интегрированную среду разработки Visual Studio для установки свойств проекта и вызова MSBuild. Изменение файлов проекта вручную может привести к серьезным проблемам, если они не были выполнены правильно.

Если по некоторым причинам вы хотите использовать MSBuild непосредственно из командной строки, см. раздел [Использование MSBuild из командной строки](../msbuild-visual-cpp.md). Дополнительные сведения о MSBuild см. в разделе [MSBuild](/visualstudio/msbuild/msbuild) в документации по Visual Studio.

## <a name="in-this-section"></a>В этом разделе

[Внутренние компоненты MSBuild для проектов C++](msbuild-visual-cpp-overview.md)<br/>
Сведения о хранении и использовании свойств и целевых объектов.

[Стандартные макросы для команд и свойств сборки](common-macros-for-build-commands-and-properties.md)<br/>
Описывает макросы (константы времени компиляции), которые можно использовать для определения таких свойств, как пути и версии продукта.

[Типы файлов, созданные для проектов C++](file-types-created-for-visual-cpp-projects.md)<br/>
Описывает различные типы файлов, создаваемые Visual Studio для различных типов проектов.

[Шаблоны проектов Visual Studio C++](visual-cpp-project-types.md)<br>
Описывает типы проектов на основе MSBuild, доступные для C++.

[Новые шаблоны элементов C++](using-visual-cpp-add-new-item-templates.md)<br>
Описывает исходные файлы и другие элементы, которые можно добавить в проект Visual Studio.

[Файлы предкомпилированных заголовков](../creating-precompiled-header-files.md) Использование предварительно скомпилированных файлов заголовков и создание собственного пользовательского предкомпилированного кода для ускорения времени сборки.

[Справочник по свойствам проекта Visual Studio](property-pages-visual-cpp.md)<br/>
Справочная документация по свойствам проекта, заданным в интегрированной среде разработки Visual Studio.

## <a name="see-also"></a>См. также

[Справочные сведения о сборке C/C++](c-cpp-building-reference.md)
