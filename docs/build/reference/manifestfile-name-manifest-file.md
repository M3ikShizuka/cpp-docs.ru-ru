---
description: Дополнительные сведения о:/MANIFESTFILE (имя файла манифеста)
title: /MANIFESTFILE (Имя файла манифеста)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.ManifestFile
helpviewer_keywords:
- MANIFESTFILE linker option
- -MANIFESTFILE linker option
- /MANIFESTFILE linker option
ms.assetid: befa5ab2-a9cf-4c9b-969a-e7b4a930f08d
ms.openlocfilehash: a0d3a4ba1d17c4aa8c97cb09cc768e614e46c864
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97138025"
---
# <a name="manifestfile-name-manifest-file"></a>/MANIFESTFILE (Имя файла манифеста)

```
/MANIFESTFILE:filename
```

## <a name="remarks"></a>Комментарии

/MANIFESTFILE позволяет изменить имя файла манифеста по умолчанию.  Имя файла манифеста по умолчанию — это имя файла с добавленным расширением MANIFEST.

/MANIFESTFILE не будет действовать, если не связать с [/manifest](manifest-create-side-by-side-assembly-manifest.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Разверните узел **Свойства конфигурации**.

1. Разверните узел **Компоновщик**.

1. Выберите страницу свойств **файл манифеста** .

1. Измените свойство **файла манифеста** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ManifestFile%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
