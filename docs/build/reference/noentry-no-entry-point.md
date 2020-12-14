---
description: Дополнительные сведения о:/NOENTRY (без точки входа)
title: /NOENTRY (точка входа отсутствует)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.ResourceOnlyDLL
- /noentry
helpviewer_keywords:
- entry points [C++], linker specifying
- -NOENTRY linker option
- resource-only DLLs [C++], creating
- NOENTRY linker option
- /NOENTRY linker option [C++]
- DLLs [C++], creating
ms.assetid: 0214dd41-35ad-43ab-b892-e636e038621a
ms.openlocfilehash: c3d1f725a4e185a052d443010894ff2dc2261675
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97196689"
---
# <a name="noentry-no-entry-point"></a>/NOENTRY (точка входа отсутствует)

```
/NOENTRY
```

## <a name="remarks"></a>Комментарии

Параметр /NOENTRY требуется для создания DLL-библиотеки, содержащей только ресурсы, без исполняемого кода. Дополнительные сведения см. [в разделе создание Resource-Only DLL](../creating-a-resource-only-dll.md).

Используйте этот параметр, чтобы LINK не добавлял ссылку на `_main` в DLL.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **Компоновщик** .

1. Выберите страницу свойств **Дополнительно**.

1. Измените свойство **без точки входа** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ResourceOnlyDLL%2A>.

## <a name="see-also"></a>См. также раздел

[Создание Resource-Only DLL](../creating-a-resource-only-dll.md)<br/>
[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
