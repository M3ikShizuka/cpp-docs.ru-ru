---
description: Дополнительные сведения о:/GE (Включение проверок стека)
title: /Ge (включить проверку стека)
ms.date: 11/04/2016
f1_keywords:
- /ge
helpviewer_keywords:
- -Ge compiler option [C++]
- enable stack probes
- /Ge compiler option [C++]
- stack, stack probes
- stack probes
- stack checking calls
- Ge compiler option [C++]
ms.assetid: 4b54deae-4e3c-4bfa-95f3-ba23590f7258
ms.openlocfilehash: db996deb1c5b964661e5465fe72cfb0fab93df56
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192022"
---
# <a name="ge-enable-stack-probes"></a>/Ge (включить проверку стека)

Активирует зонды стека для каждого вызова функции, для которого требуется хранилище локальных переменных.

## <a name="syntax"></a>Синтаксис

```
/Ge
```

## <a name="remarks"></a>Remarks

Этот механизм полезен при перезаписи функций проверки стека. Рекомендуется использовать [/GH (включить функцию-обработчик _penter)](gh-enable-penter-hook-function.md) вместо перезаписи проверки стека.

[/GS (управление вызовами проверки стека)](gs-control-stack-checking-calls.md) действует одинаково.

**/GE** является устаревшим; начиная с Visual Studio 2005, компилятор автоматически создает проверку стека. Список устаревших параметров компилятора см. в разделе **устаревшие и удаленные параметры** компилятора в [параметрах компилятора, перечисленных по категориям](compiler-options-listed-by-category.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
