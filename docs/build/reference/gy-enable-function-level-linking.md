---
description: Дополнительные сведения о:/Gy (включение связывания Function-Level)
title: /Gy (включение компоновки на уровне функций)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLCompilerTool.EnableFunctionLevelLinking
- /gy
- VC.Project.VCCLWCECompilerTool.EnableFunctionLevelLinking
helpviewer_keywords:
- enable function-level linking compiler option [C++]
- COMDAT function
- Gy compiler option [C++]
- -Gy compiler option [C++]
- /Gy compiler option [C++]
- packaged functions
ms.assetid: 0d3cf14c-ed7d-4ad3-b4b6-104e56f61046
ms.openlocfilehash: 3c4136b25001f7f6d6729b9c6089995d1bcd71bf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200134"
---
# <a name="gy-enable-function-level-linking"></a>/Gy (включение компоновки на уровне функций)

Компилятор может упаковывать отдельные функции в форме упакованных функций (COMDAT).

## <a name="syntax"></a>Синтаксис

```
/Gy[-]
```

## <a name="remarks"></a>Remarks

Компоновщик требует, чтобы функции были упакованы отдельно как COMDAT для исключения или упорядочивания отдельных функций в DLL-файле или exe.

Можно использовать параметр компоновщика [/OPT (оптимизация)](opt-optimizations.md) , чтобы исключить из EXE-файла пакетные функции, которые не ссылаются.

Для включения упакованных функций в указанный порядок в exe-файле можно использовать параметр компоновщика [/Order (размещение функций по порядку)](order-put-functions-in-order.md) .

Встроенные функции всегда упаковываются, если они создаются как вызовы (например, если встраивание отключено или вы принимаете адрес функции). Кроме того, функции элементов C++, определенные в объявлении класса, автоматически упаковываются; другие функции — нет, и выбор этого параметра необходим для компиляции их в виде упакованных функций.

> [!NOTE]
> Параметр [/Zi](z7-zi-zi-debug-information-format.md) , используемый для функции "изменить и продолжить", автоматически задает параметр **/Gy** .

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Перейдите на страницу свойств **Создание кода** .

1. Измените свойство **включить связывание Function-Level** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.EnableFunctionLevelLinking%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
