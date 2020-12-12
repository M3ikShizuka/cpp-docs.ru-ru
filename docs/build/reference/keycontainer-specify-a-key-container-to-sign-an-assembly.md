---
description: Дополнительные сведения о параметре/KEYCONTAINER (указание контейнера ключей для подписи сборки)
title: /KEYCONTAINER (задание контейнера ключей для подписи сборки)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.KeyContainer
- /keycontainer
helpviewer_keywords:
- KEYCONTAINER linker option
- /KEYCONTAINER linker option
- -KEYCONTAINER linker option
ms.assetid: 94882d12-b77a-49c7-96d0-18a31aee001e
ms.openlocfilehash: 5f32fdc5400103d4038139fa2dfe9409c9740236
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199588"
---
# <a name="keycontainer-specify-a-key-container-to-sign-an-assembly"></a>/KEYCONTAINER (задание контейнера ключей для подписи сборки)

```
/KEYCONTAINER:name
```

## <a name="arguments"></a>Аргументы

*name*<br/>
Контейнер, содержащий ключ. Поместите строку в двойные кавычки (""), если она содержит пробел.

## <a name="remarks"></a>Комментарии

Компоновщик создает подписанную сборку, вставляя открытый ключ в манифест сборки и подписывая окончательную сборку с закрытым ключом. Чтобы создать файл ключа, введите в командной строке команду [sn-k](/dotnet/framework/tools/sn-exe-strong-name-tool) *filename* . **sn-i** устанавливает пару ключей в контейнер.

При компиляции с параметром [/LN](ln-create-msil-module.md)имя файла ключа сохраняется в модуле и включается в сборку, созданную при компиляции сборки, содержащей явную ссылку на модуль, через [#using](../../preprocessor/hash-using-directive-cpp.md)или при компоновке с помощью [/ASSEMBLYMODULE](assemblymodule-add-a-msil-module-to-the-assembly.md).

Также можно передать сведения о шифровании компилятору с параметром [/keyfile](keyfile-specify-key-or-key-pair-to-sign-an-assembly.md). Если требуется частично подписанная сборка, используйте параметр [/delaysign](delaysign-partially-sign-an-assembly.md) . Дополнительные сведения о подписывании сборки см. в разделе [сборки со строгими именами (подписывание сборок) (C++/CLI)](../../dotnet/strong-name-assemblies-assembly-signing-cpp-cli.md) .

Другие параметры компоновщика, влияющие на создание сборки:

- [/ASSEMBLYDEBUG](assemblydebug-add-debuggableattribute.md)

- [/ASSEMBLYLINKRESOURCE](assemblylinkresource-link-to-dotnet-framework-resource.md)

- [/ASSEMBLYMODULE](assemblymodule-add-a-msil-module-to-the-assembly.md)

- [/ASSEMBLYRESOURCE](assemblyresource-embed-a-managed-resource.md)

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
