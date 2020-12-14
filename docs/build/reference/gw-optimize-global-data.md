---
description: Дополнительные сведения о:/GW (Оптимизация глобальных данных)
title: /Gw (оптимизация глобальных данных)
ms.date: 11/04/2016
f1_keywords:
- /Gw
helpviewer_keywords:
- /Gw compiler option [C++]
- -Gw compiler option [C++]
ms.assetid: 6f90f4e9-5eb8-4c47-886e-631278a5a4a9
ms.openlocfilehash: 2f9a6b9452f09473e650a5453ad2600cc73f0c00
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200147"
---
# <a name="gw-optimize-global-data"></a>/Gw (оптимизация глобальных данных)

Упакуйте глобальные данные в разделы COMDAT для оптимизации.

## <a name="syntax"></a>Синтаксис

```
/Gw[-]
```

## <a name="remarks"></a>Remarks

Параметр **/GW** предписывает компилятору упаковывать глобальные данные в отдельные разделы COMDAT. По умолчанию **/GW** отключен и должен быть явно включен. Чтобы явно отключить его, используйте **/ГВ-**. Если включены оба **/GW** и [/GL](gl-whole-program-optimization.md) , компоновщик использует оптимизацию всей программы для сравнения разделов COMDAT по нескольким файловым файлам, чтобы исключить неиспользуемые глобальные данные или объединить одинаковые глобальные данные только для чтения. Это может значительно уменьшить размер результирующего двоичного исполняемого файла.

При отдельном компилировании и компоновке можно использовать параметр компоновщика [/OPT: REF](opt-optimizations.md) для исключения из исполняемого файла неиспользованных глобальных данных в объектных файлах, скомпилированных с параметром **/GW** .

Параметры компоновщика [/OPT: ICF](opt-optimizations.md) и [/LTCG](ltcg-link-time-code-generation.md) можно использовать совместно для слияния в исполняемом файле всех идентичных глобальных данных, предназначенных только для чтения, в нескольких объектных файлах, скомпилированных с помощью параметра **/GW** .

Дополнительные сведения см. в разделе [Введение в параметр компилятора/GW](https://devblogs.microsoft.com/cppblog/introducing-gw-compiler-switch/) в блоге группы разработчиков C++.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Измените свойство **Дополнительные параметры** , включив в него **/GW** , а затем нажмите кнопку **ОК**.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
