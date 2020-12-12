---
description: Дополнительные сведения о:/homeparams (копирование параметров реестра в стек)
title: /homeparams (копирование параметров регистров в стек)
ms.date: 12/17/2018
f1_keywords:
- /homeparams
helpviewer_keywords:
- /homeparams compiler option [C++]
- -homeparams compiler option [C++]
ms.assetid: 51067de4-24f7-436b-b8d9-bc867a7d53aa
ms.openlocfilehash: 52145534121831be256c3db2a6ccacdffb30b2c2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191476"
---
# <a name="homeparams-copy-register-parameters-to-stack"></a>/homeparams (копирование параметров регистров в стек)

Принудительно записывает параметры, переданные в регистры, в их расположение в стеке после ввода функции.

## <a name="syntax"></a>Синтаксис

> **/homeparams**

## <a name="remarks"></a>Комментарии

Этот параметр компилятора доступен только в машинных и перекрестных компиляторах, предназначенных для x64.

Соглашение о вызовах x64 требует выделения пространства стека для всех параметров, даже для параметров, передаваемых в регистрах. Дополнительные сведения см. в разделе [Передача параметров](../../build/x64-calling-convention.md#parameter-passing). По умолчанию параметры регистра не копируются в пространство стека, выделенное для них в сборках выпуска. Это затрудняет отладку оптимизированной сборки выпуска программы.

Для сборок выпуска можно использовать параметр **/homeparams** , чтобы заставить компилятор копировать параметры реестра в стек, чтобы обеспечить возможность отладки приложения. **/homeparams** подразумевает недостаток производительности, так как требует дополнительного цикла для загрузки параметров регистров в стек.

В отладочных сборках стек всегда заполняется параметрами, передаваемыми в регистрах.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте страницу свойств **конфигурации**  >  **C/C++**  >  **Командная строка** .

1. В поле **Дополнительные параметры** введите параметр компилятора.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
