---
description: Дополнительные сведения о:/ASSEMBLYLINKRESOURCE (ссылка на ресурс .NET Framework)
title: Параметр /ASSEMBLYLINKRESOURCE (ссылка на ресурс .NET Framework)
ms.date: 11/04/2016
f1_keywords:
- /ASSEMBLYLINKRESOURCE
- VC.Project.VCLinkerTool.AssemblyLinkResource
helpviewer_keywords:
- -ASSEMBLYLINKRESOURCE linker option
- ASSEMBLYLINKRESOURCE linker option
- /ASSEMBLYLINKRESOURCE linker option
ms.assetid: 8b6ad184-1b33-47a4-8513-4803cf915b64
ms.openlocfilehash: 32761cb16e8428d5e3c18330dffb49a50a42903c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97183013"
---
# <a name="assemblylinkresource-link-to-net-framework-resource"></a>Параметр /ASSEMBLYLINKRESOURCE (ссылка на ресурс .NET Framework)

```
/ASSEMBLYLINKRESOURCE:filename
```

## <a name="arguments"></a>Аргументы

*filename*<br/>
Файл ресурсов .NET Framework, ссылку на который необходимо создать из сборки.

## <a name="remarks"></a>Комментарии

Параметр/ASSEMBLYLINKRESOURCE создает ссылку на ресурс .NET Framework в выходном файле. файл ресурсов не помещается в выходной файл. [/ASSEMBLYRESOURCE](assemblyresource-embed-a-managed-resource.md) внедряет файл ресурсов в выходной файл.

Связанные ресурсы являются общедоступными в сборке при их создании с помощью компоновщика.

Для/ASSEMBLYLINKRESOURCE требуется, чтобы компиляция включала [/CLR](clr-common-language-runtime-compilation.md); Не допускается использование [/LN](ln-create-msil-module.md) или [/NOASSEMBLY](noassembly-create-a-msil-module.md) с/ассемблилинкресаурце.

Если *filename* — это .NET Framework файл ресурсов, который создается, например, [Resgen.exe](/dotnet/framework/tools/resgen-exe-resource-file-generator) или в среде разработки, доступ к нему можно получить с помощью членов пространства имен **System. Resources** . Дополнительные сведения см. в разделе [System. Resources. ResourceManager](/dotnet/api/system.resources.resourcemanager). Для всех остальных ресурсов используйте методы **жетманифестресаурце** \* в классе **System. Reflection. Assembly** для доступа к ресурсу во время выполнения.

*filename* может быть любым форматом файла. Например, может потребоваться сделать собственную DLL-библиотеку частью сборки, чтобы ее можно было установить в глобальный кэш сборок и получить к ней доступ из управляемого кода в сборке.

Другие параметры компоновщика, влияющие на создание сборки:

- [/ASSEMBLYDEBUG](assemblydebug-add-debuggableattribute.md)

- [/ASSEMBLYMODULE](assemblymodule-add-a-msil-module-to-the-assembly.md)

- [/ASSEMBLYRESOURCE](assemblyresource-embed-a-managed-resource.md)

- [/DELAYSIGN](delaysign-partially-sign-an-assembly.md)

- [/KEYCONTAINER](keycontainer-specify-a-key-container-to-sign-an-assembly.md)

- [/KEYFILE](keyfile-specify-key-or-key-pair-to-sign-an-assembly.md)

- [/NOASSEMBLY](noassembly-create-a-msil-module.md)

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр в поле **Дополнительные параметры** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
