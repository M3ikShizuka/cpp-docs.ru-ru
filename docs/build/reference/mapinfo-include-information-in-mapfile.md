---
description: Дополнительные сведения о:/MAPINFO (включение сведений в параметр сопоставления)
title: /MAPINFO (включение данных в файл сопоставления)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.MapLines
- VC.Project.VCLinkerTool.MapInfoFixups
- VC.Project.VCLinkerTool.MapExports
- /mapinfo
helpviewer_keywords:
- /MAPINFO linker option
- MAPINFO linker option
- -MAPINFO linker option
ms.assetid: 533d2bce-f9b7-4fea-ae1c-0b4864c9d10b
ms.openlocfilehash: 5cf785182bd91923c3398d542d7e60d9afdb4a4e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97137908"
---
# <a name="mapinfo-include-information-in-mapfile"></a>/MAPINFO (включение данных в файл сопоставления)

```
/MAPINFO:EXPORTS
```

## <a name="remarks"></a>Комментарии

Параметр/MAPINFO указывает компоновщику включить указанные сведения в параметр сопоставления, который создается при указании параметра [/Map](map-generate-mapfile.md) .  EXPORTs сообщает компоновщику о необходимости включения экспортированных функций.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Отладка** .

1. Изменение свойств **Map EXPORTS** :

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.MapExports%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
