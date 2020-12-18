---
description: 'Подробнее о следующем: Практическое руководство. Изменение свойств и целевых объектов проекта C++ без изменения файла проекта'
title: Практическое руководство. Изменение свойств и целевых объектов проекта C++ без изменения файла проекта
ms.date: 11/28/2018
helpviewer_keywords:
- project properties [C++], modifying outside project file
ms.openlocfilehash: 91f71ccf7764307fef174d31a63583d6a3ce2aeb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179867"
---
# <a name="how-to-modify-c-project-properties-and-targets-without-changing-the-project-file"></a>Практическое руководство. Изменение свойств и целевых объектов проекта C++ без изменения файла проекта

Вы можете переопределить свойства проекта и целевые объекты из командной строки MSBuild, не изменяя файл проекта. Это удобно в том случае, если вы хотите применять некоторые свойства лишь временно или периодически. Для этого нужно обладать некоторыми знаниями о MSBuild. Дополнительные сведения см. в разделе [MSBuild](/visualstudio/msbuild/msbuild).

> [!IMPORTANT]
> Для создания файла PROPS или TARGETS можно использовать редактор XML в Visual Studio или любой текстовый редактор. Не используйте **диспетчер свойств** в этом сценарии, так как он добавляет свойства в файл проекта.

*Переопределение свойств проекта*

1. Создайте файл PROPS, задающий свойства, которые нужно переопределить.

1. В командной строке укажите: set ForceImportBeforeCppTargets="C:\sources\my_props.props".

*Переопределение целевых объектов проекта*

1. Создайте файл TARGETS с соответствующей реализацией или конкретным целевым объектом.

2. В командной строке укажите: set ForceImportAfterCppTargets ="C:\sources\my_target.targets".

Вы также можете задать любой параметр в командной строке MSBuild с помощью параметра "/p:".

```cmd
> msbuild myproject.sln /p:ForceImportBeforeCppTargets="C:\sources\my_props.props"
> msbuild myproject.sln /p:ForceImportAfterCppTargets="C:\sources\my_target.targets"
```

В этом случае переопределение свойств и целевых объектов эквивалентно добавлению следующих операций импорта во все файлы VCXPROJ в решении.

```cmd
<Import Project=="C:\sources\my_props.props" />
<Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
<Import Project==" C:\sources\my_target.targets"" />
```
