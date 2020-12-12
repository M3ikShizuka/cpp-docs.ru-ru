---
description: Дополнительные сведения о:/Arch (ARM)
title: /arch (ARM)
ms.date: 11/04/2016
ms.assetid: 4f1406ff-f174-487c-a126-8ab06cf447c1
ms.openlocfilehash: 885b624eb6a470d24d691641d0be63515ee76a49
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179568"
---
# <a name="arch-arm"></a>/arch (ARM)

Указывает архитектуру для создания кода на платформе ARM. См. также [/Arch (x86)](arch-x86.md) и [/Arch (x64)](arch-x64.md).

## <a name="syntax"></a>Синтаксис

```
/arch:[ARMv7VE|VFPv4]
```

## <a name="arguments"></a>Аргументы

**/Arch: ARMv7VE**<br/>
Включает использование инструкций расширения виртуализации ARMv7VE.

**/Arch: VFPv4**<br/>
Включает использование инструкций ARM VFPv4. Если этот параметр не указан, по умолчанию используется VFPv3.

## <a name="remarks"></a>Комментарии

`_M_ARM_FP`Макрос (только для ARM) указывает, какой параметр компилятора (если  таковой имеется) был использован. Для получения дополнительной информации см. [Predefined Macros](../../preprocessor/predefined-macros.md).

При использовании [параметра/clr](clr-common-language-runtime-compilation.md) для компиляции **/Arch** не влияет на создание кода для управляемых функций. **/Arch** влияет только на создание кода для собственных функций.

### <a name="to-set-the-archarmv7ve-or-archvfpv4-compiler-option-in-visual-studio"></a>Чтобы задать параметр компилятора /arch:ARMv7VE или /arch:VFPv4 в Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойств сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. В поле **Дополнительные параметры** добавьте `/arch:ARMv7VE` или `/arch:VFPv4` .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.EnableEnhancedInstructionSet%2A>.

## <a name="see-also"></a>См. также раздел

[/Arch (минимальная архитектура ЦП)](arch-minimum-cpu-architecture.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
