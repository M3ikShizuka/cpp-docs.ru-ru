---
description: Дополнительные сведения о:/OD (Disable (Отладка))
title: /Od (Выключение (отладчика))
ms.date: 11/04/2016
f1_keywords:
- /od
helpviewer_keywords:
- no optimizations
- fast compiling
- /Od compiler option [C++]
- disable optimizations
- Od compiler option [C++]
- -Od compiler option [C++]
- disable (debug) compiler option [C++]
ms.assetid: b1ac31b7-e086-4eeb-be5e-488f7513f5f5
ms.openlocfilehash: 9d425244a1790a9bb74e1c92db88f32bb0372ab2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97214309"
---
# <a name="od-disable-debug"></a>/Od (Выключение (отладчика))

Отключает все оптимизации в программе и ускоряет компиляцию.

## <a name="syntax"></a>Синтаксис

```
/Od
```

## <a name="remarks"></a>Remarks

Это значение по умолчанию. Поскольку **/OD** подавляет перемещение кода, это упрощает процесс отладки. Дополнительные сведения о параметрах компилятора для отладки см. в разделе [/Z7,/Zi,/Zi (формат отладочной информации)](z7-zi-zi-debug-information-format.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Перейдите на страницу свойств **Оптимизация** .

1. Измените свойство **Оптимизация** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.Optimization%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры/o (оптимизация кода)](o-options-optimize-code.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
[/Z7,/Zi,/ZI (формат отладочной информации)](z7-zi-zi-debug-information-format.md)
