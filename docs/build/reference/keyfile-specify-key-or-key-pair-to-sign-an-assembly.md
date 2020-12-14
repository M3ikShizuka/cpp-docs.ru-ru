---
description: Дополнительные сведения о:/KEYFILE (указание ключа или пары ключей для подписи сборки)
title: /KEYFILE (задание ключа или пары ключей для подписи сборки)
ms.date: 11/04/2016
f1_keywords:
- /keyfile
- VC.Project.VCLinkerTool.KeyFile
helpviewer_keywords:
- /KEYFILE linker option
- -KEYFILE linker option
- KEYFILE linker option
ms.assetid: 9b71f8c0-541c-4fe5-a0c7-9364f42ecb06
ms.openlocfilehash: 23c4962ab57688f5d8c1af27fd412d7d36be01a0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191164"
---
# <a name="keyfile-specify-key-or-key-pair-to-sign-an-assembly"></a>/KEYFILE (задание ключа или пары ключей для подписи сборки)

```
/KEYFILE:filename
```

## <a name="arguments"></a>Аргументы

*filename*<br/>
Файл, который содержит ключ. Поместите строку в двойные кавычки (""), если она содержит пробел.

## <a name="remarks"></a>Комментарии

Компоновщик вставляет открытый ключ в манифест сборки, а затем подписывает окончательную сборку закрытым ключом. Чтобы создать файл ключа, введите в командной строке команду [sn-k](/dotnet/framework/tools/sn-exe-strong-name-tool) *filename* . Подписанная сборка называется строгим именем.

При компиляции с параметром [/LN](ln-create-msil-module.md)имя файла ключа сохраняется в модуле и включается в сборку, созданную при компиляции сборки, содержащей явную ссылку на модуль, через [#using](../../preprocessor/hash-using-directive-cpp.md)или при компоновке с помощью [/ASSEMBLYMODULE](assemblymodule-add-a-msil-module-to-the-assembly.md).

Также можно передать сведения о шифровании компоновщику с параметром [/keycontainer](keycontainer-specify-a-key-container-to-sign-an-assembly.md). Если требуется частично подписанная сборка, используйте параметр [/delaysign](delaysign-partially-sign-an-assembly.md) . Дополнительные сведения о подписывании сборки см. в разделе [сборки со строгими именами (подписывание сборок) (C++/CLI)](../../dotnet/strong-name-assemblies-assembly-signing-cpp-cli.md) .

Если указаны параметры **/keyfile** и **/keycontainer** (либо параметр командной строки, либо настраиваемый атрибут), то компоновщик сначала попытается попытаться контейнер ключей. В случае успеха сборка подписывается данными контейнера ключей. Если компоновщик не находит контейнер ключей, он попытается выполнить файл, указанный параметром/КЭЙФИЛЕ. В случае успеха сборка подписывается данными из файла ключей, и эти данные о ключах будут помещены в контейнер ключей (аналогично команде sn -i); таким образом, при следующей компиляции контейнер ключей будет действителен.

Обратите внимание, что файл ключей может содержать только открытый ключ.

Дополнительные сведения см. в статье [Создание и использование сборок со строгими именами](/dotnet/framework/app-domains/create-and-use-strong-named-assemblies).

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
