---
description: Дополнительные сведения о программе:/DEF (указание файла Module-Definition)
title: /DEF (указание файла определения модуля)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.ModuleDefinitionFile
- /def
helpviewer_keywords:
- module definition files, specifying
- DEF linker option
- -DEF linker option
- module definition files
- /DEF linker option
ms.assetid: 6497fa68-65f0-48ca-8f66-b87166fc631a
ms.openlocfilehash: 3b9178004621a55f999f7c2636eaa5b697d2de98
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201707"
---
# <a name="def-specify-module-definition-file"></a>/DEF (указание файла определения модуля)

```
/DEF:filename
```

## <a name="arguments"></a>Аргументы

*filename*<br/>
Имя файла определения модуля (DEF), передаваемого компоновщику.

## <a name="remarks"></a>Комментарии

Параметр/DEF передает файл определения модуля (DEF) компоновщику. Для ссылки можно указать только один DEF – файл. Дополнительные сведения о DEF-файлах см. в разделе [файлы определения модуля](module-definition-dot-def-files.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **входные данные** .

1. Измените свойство **файла определения модуля** .

Чтобы указать DEF-файл в среде разработки, добавьте его в проект вместе с другими файлами, а затем укажите файл в параметре/DEF.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ModuleDefinitionFile%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
