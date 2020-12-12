---
description: Дополнительные сведения о:/ASSEMBLYRESOURCE (внедрение управляемого ресурса)
title: /ASSEMBLYRESOURCE (внедрение управляемого ресурса)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.EmbedManagedResourceFile
- /ASSEMBLYRESOURCE
helpviewer_keywords:
- ASSEMBLYRESOURCE linker option
- assemblies [C++]
- -ASSEMBLYRESOURCE linker option
- assemblies [C++], linking resource files
- /ASSEMBLYRESOURCE linker option
ms.assetid: 0ce6e1fb-921b-4b1b-a59c-d35388d789f2
ms.openlocfilehash: 3f79cc177df72bb83288a0a229fdf47adb0e7fc0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97182922"
---
# <a name="assemblyresource-embed-a-managed-resource"></a>/ASSEMBLYRESOURCE (внедрение управляемого ресурса)

```
/ASSEMBLYRESOURCE:filename[,[name][,PRIVATE]]
```

## <a name="parameters"></a>Параметры

*filename*<br/>
Управляемый ресурс, который необходимо внедрить в эту сборку.

*name*<br/>
Необязательный элемент. Логическое имя для ресурса; имя, используемое для загрузки ресурса. По умолчанию используется имя файла.

При необходимости можно указать, должен ли файл быть частным в манифесте сборки. По умолчанию *имя* является общедоступным в сборке.

## <a name="remarks"></a>Комментарии

Используйте параметр/ASSEMBLYRESOURCE для внедрения ресурса в сборку.

Ресурсы являются общедоступными в сборке при их создании с помощью компоновщика. Компоновщик не позволяет переименовать ресурс в сборке.

Если *filename* — файл ресурсов .NET Framework (Resources), созданный, например, [генератор файлов ресурсов (Resgen.exe)](/dotnet/framework/tools/resgen-exe-resource-file-generator) или в среде разработки, доступ к нему можно получить с помощью членов пространства имен **System. Resources** (Дополнительные сведения см. в разделе [System. Resources. ResourceManager](/dotnet/api/system.resources.resourcemanager) ). Для всех остальных ресурсов используйте методы **жетманифестресаурце** \* в классе **System. Reflection. Assembly** для доступа к ресурсу во время выполнения.

Другие параметры компоновщика, влияющие на создание сборки:

- [/ASSEMBLYDEBUG](assemblydebug-add-debuggableattribute.md)

- [/ASSEMBLYLINKRESOURCE](assemblylinkresource-link-to-dotnet-framework-resource.md)

- [/ASSEMBLYMODULE](assemblymodule-add-a-msil-module-to-the-assembly.md)

- [/DELAYSIGN](delaysign-partially-sign-an-assembly.md)

- [/KEYFILE](keyfile-specify-key-or-key-pair-to-sign-an-assembly.md)

- [/KEYCONTAINER](keycontainer-specify-a-key-container-to-sign-an-assembly.md)

- [/NOASSEMBLY](noassembly-create-a-msil-module.md)

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **входные данные** .

1. Измените свойство **внедрить управляемый файл ресурсов** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.EmbedManagedResourceFile%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
