---
description: Дополнительные сведения о:/DELAYSIGN (частичное подписание сборки)
title: /DELAYSIGN (частичное подписание сборки)
ms.date: 11/04/2016
f1_keywords:
- /delaysign
- VC.Project.VCLinkerTool.DelaySign
helpviewer_keywords:
- /DELAYSIGN linker option
- DELAYSIGN linker option
- -DELAYSIGN linker option
ms.assetid: 15244d30-3ecb-492f-a408-ffe81f38de20
ms.openlocfilehash: 40eeaef958b6a188fd4739fcdc0f5ef5123b220a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201486"
---
# <a name="delaysign-partially-sign-an-assembly"></a>/DELAYSIGN (частичное подписание сборки)

```
/DELAYSIGN[:NO]
```

## <a name="arguments"></a>Аргументы

**NO**<br/>
Указывает, что сборка не должна быть частично подписана.

## <a name="remarks"></a>Комментарии

Используйте параметр **/delaysign** , если хотите поместить только открытый ключ в сборку. Значение по умолчанию — **/delaysign: No**.

Параметр **/delaysign** не действует, если не используется с [/keyfile](keyfile-specify-key-or-key-pair-to-sign-an-assembly.md) или [/keycontainer](keycontainer-specify-a-key-container-to-sign-an-assembly.md).

При запросе полностью подписанной сборки компилятор хэширует файл, содержащий манифест (метаданные сборки), и подписывает хэш закрытым ключом. Итоговая цифровая подпись хранится в файле, содержащем манифест. Если сборка имеет отложенную подпись, компоновщик не выполняет вычисление и сохранение подписи, но резервирует место в файле, чтобы подпись можно было добавить позже.

Например, использование **/delaysign** позволяет инженеру-тестировщику разместить сборку в глобальном кэше. После тестирования можно полностью подписать сборку, поместив закрытый ключ в сборку.

Дополнительные сведения о подписывании сборки см. в разделе [сборки со строгими именами (подписывание сборок) (C++/CLI](../../dotnet/strong-name-assemblies-assembly-signing-cpp-cli.md) ) и [Отложенная подпись сборки](/dotnet/framework/app-domains/delay-sign-assembly) .

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
