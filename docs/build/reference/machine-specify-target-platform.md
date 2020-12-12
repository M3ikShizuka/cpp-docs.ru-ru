---
description: Дополнительные сведения о:/MACHINE (Указание целевой платформы)
title: Параметр /MACHINE (определение целевой платформы)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.TargetMachine
- /machine
helpviewer_keywords:
- mapfiles, creating linker
- target platform
- -MACHINE linker option
- /MACHINE linker option
- MACHINE linker option
ms.assetid: 8d41bf4b-7e53-4ab9-9085-d852b08d31c2
ms.openlocfilehash: a1bf87142fb99577672391356a43a2771ea0b09f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190813"
---
# <a name="machine-specify-target-platform"></a>Параметр /MACHINE (определение целевой платформы)

```
/MACHINE:{ARM|EBC|X64|X86}
```

## <a name="remarks"></a>Комментарии

Параметр/MACHINE указывает целевую платформу для программы.

Как правило, не нужно указывать параметр/MACHINE. LINK выводит тип компьютера из OBJ-файлов. Однако в некоторых случаях LINK не может определить тип компьютера и выдает [ошибку средств компоновщика LNK1113](../../error-messages/tool-errors/linker-tools-error-lnk1113.md). При возникновении такой ошибки укажите/МАЧИНЕ..

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Дополнительно** .

1. Измените свойство **целевого компьютера** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.TargetMachine%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
