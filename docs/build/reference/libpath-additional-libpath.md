---
description: Дополнительные сведения:/LIBPATH (дополнительный параметр libpath)
title: Параметр /LIBPATH (дополнительный параметр libpath)
ms.date: 11/04/2016
f1_keywords:
- /libpath
- VC.Project.VCLinkerTool.AdditionalLibraryDirectories
helpviewer_keywords:
- LIBPATH linker option
- /LIBPATH linker option
- Additional Libpath linker option
- environment library path override
- -LIBPATH linker option
- library path linker option
ms.assetid: 7240af0b-9a3d-4d53-8169-2a92cd6958ba
ms.openlocfilehash: 5db7a0f80cb741a65bac5a4dbb7fd79e28b67459
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191034"
---
# <a name="libpath-additional-libpath"></a>Параметр /LIBPATH (дополнительный параметр libpath)

```
/LIBPATH:dir
```

## <a name="parameters"></a>Параметры

*dir*<br/>
Указывает путь, который будет искать компоновщик перед поиском пути, указанного в параметре среды LIB.

## <a name="remarks"></a>Комментарии

Используйте параметр/LIBPATH, чтобы переопределить путь к библиотеке среды. Компоновщик сначала будет искать по пути, указанному этим параметром, а затем искать по пути, указанному в переменной среды LIB. Для каждого введенного параметра/LIBPATH можно указать только один каталог. Если необходимо указать более одного каталога, необходимо указать несколько параметров/LIBPATH. Компоновщик будет выполнять поиск по указанным каталогам по порядку.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Общие** .

1. Измените свойство **Дополнительные каталоги библиотек** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalLibraryDirectories%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
