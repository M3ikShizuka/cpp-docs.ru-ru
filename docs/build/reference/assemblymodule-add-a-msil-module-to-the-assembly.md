---
description: Дополнительные сведения о:/ASSEMBLYMODULE (Добавление модуля MSIL в сборку)
title: /ASSEMBLYMODULE (добавление модуля MSIL в сборку)
ms.date: 11/04/2016
f1_keywords:
- /assemblymodule
- VC.Project.VCLinkerTool.AddModuleNamesToAssembly
helpviewer_keywords:
- ASSEMBLYMODULE linker option
- assemblies [C++], adding modules to
- assemblies [C++]
- /ASSEMBLYMODULE linker option
- -ASSEMBLYMODULE linker option
ms.assetid: 67357da8-e4b6-49fd-932c-329a5777f143
ms.openlocfilehash: d56895b6bec05efda1104e319e93a040f818e06e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97182948"
---
# <a name="assemblymodule-add-a-msil-module-to-the-assembly"></a>/ASSEMBLYMODULE (добавление модуля MSIL в сборку)

```
/ASSEMBLYMODULE:filename
```

## <a name="arguments"></a>Аргументы

*filename*<br/>
Модуль, который необходимо включить в эту сборку.

## <a name="remarks"></a>Комментарии

Параметр/ASSEMBLYMODULE позволяет добавить ссылку на модуль в сборку. Сведения о типе в модуле не будут доступны программе сборки, которая добавила ссылку на модуль. Однако сведения о типе в модуле будут доступны любой программе, которая ссылается на сборку.

Используйте [#using](../../preprocessor/hash-using-directive-cpp.md) , чтобы добавить ссылку на модуль в сборку и сделать сведения о типе модуля доступными для программы сборки.

Например, рассмотрим следующий сценарий.

1. Создание модуля с параметром [/LN](ln-create-msil-module.md).

1. Используйте/ASSEMBLYMODULE в другом проекте, чтобы включить модуль в текущую компиляцию, который создаст сборку. Этот проект не будет ссылаться на модуль с помощью `#using` .

1. Любой проект, который ссылается на эту сборку, теперь также может использовать типы из модуля.

Другие параметры компоновщика, влияющие на создание сборки:

- [/ASSEMBLYDEBUG](assemblydebug-add-debuggableattribute.md)

- [/ASSEMBLYLINKRESOURCE](assemblylinkresource-link-to-dotnet-framework-resource.md)

- [/ASSEMBLYRESOURCE](assemblyresource-embed-a-managed-resource.md)

- [/DELAYSIGN](delaysign-partially-sign-an-assembly.md)

- [/NOASSEMBLY](noassembly-create-a-msil-module.md)

- [/KEYFILE](keyfile-specify-key-or-key-pair-to-sign-an-assembly.md)

- [/KEYCONTAINER](keycontainer-specify-a-key-container-to-sign-an-assembly.md)

Компоновщик КОМПИЛЯТОРОМ MSVC принимает файлы NETMODULE в качестве входных данных, а выходной файл, создаваемый компоновщиком, будет сборкой или файлом. netmodule без зависимости времени выполнения ни с одним из файлов NETMODULE, которые были введены компоновщиком.  Дополнительные сведения см. в разделе [NETMODULE-файлы в качестве входных файлов компоновщика](netmodule-files-as-linker-input.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **входные данные** .

1. Измените свойство **Добавить модуль в сборку** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AddModuleNamesToAssembly%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
