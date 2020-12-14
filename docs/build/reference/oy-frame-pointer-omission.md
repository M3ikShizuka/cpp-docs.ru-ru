---
description: Дополнительные сведения о:/Oy (подавление указателей кадров)
title: /Oy (подавление указателей фрейма)
ms.date: 11/19/2018
f1_keywords:
- VC.Project.VCCLCompilerTool.OmitFramePointers
- /oy
helpviewer_keywords:
- omit frame pointer
- Oy compiler option [C++]
- stack frame pointer compiler option [C++]
- -Oy compiler option [C++]
- frame pointer omission compiler option [C++]
- suppress frame pointer creation
- /Oy compiler option [C++]
ms.assetid: c451da86-5297-4c5a-92bc-561d41379853
ms.openlocfilehash: dc0f9272bce5ad36840eac9ccdfc7e2465f7e3c3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226302"
---
# <a name="oy-frame-pointer-omission"></a>/Oy (подавление указателей фрейма)

Отменяет создание указателей на фреймы в стеке вызовов.

## <a name="syntax"></a>Синтаксис

> /Oy [-]

## <a name="remarks"></a>Комментарии

Этот параметр повышает скорость вызова функций, поскольку при этом не требуется создавать и удалять указатели фрейма. Также освобождается еще один регистр для общего использования.

**/Oy** включает подавление указателей кадров и **/ой-** отключает пропуск. В компиляторах x64, **/Oy** и **/ой-** недоступны.

Если для кода требуется адресация на основе кадров, можно указать параметр **/ой-** после параметра **/Ox** или использовать [optimize](../../preprocessor/optimize.md) с аргументами "**y**" и " **Off** ", чтобы получить максимальную оптимизацию с адресацией на основе кадров. Компилятор обнаруживает большинство ситуаций, в которых требуется адресация на основе кадров (например, с `_alloca` функциями и `setjmp` и структурной обработкой исключений).

Параметры [/Ox (включение большинства быстрых оптимизаций)](ox-full-optimization.md) и [/O1,/O2 (минимальный размер, максимизировать скорость)](o1-o2-minimize-size-maximize-speed.md) подразумевают **/Oy**. Указание **/ой-** после параметра **/Ox**, **/O1** или **/O2** отключает **/Oy**, является ли он явным или подразумеваемым.

Параметр компилятора **/Oy** делает использование отладчика более сложным, поскольку компилятор подавляет сведения о указателе на фреймы. Если задан параметр компилятора отладки ([/Z7,/Zi,/Zi](z7-zi-zi-debug-information-format.md)), рекомендуется указать параметр **/ой-** после любых других параметров компилятора оптимизации.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите   >  страницу свойств «Оптимизация **C/C++**» свойств конфигурации  >   .

1. Измените свойство " **опустить указатели кадров** ". Это свойство добавляет или удаляет только параметр **/Oy** . Если вы хотите добавить параметр **/ой-** , выберите страницу свойства **Командная строка** и измените **Дополнительные параметры**.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.OmitFramePointers%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры/o (оптимизация кода)](o-options-optimize-code.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
