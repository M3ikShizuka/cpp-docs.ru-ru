---
description: Дополнительные сведения о:/I (дополнительные каталоги включаемых каталогов)
title: /I (дополнительные каталоги включения)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLWCECompilerTool.AdditionalIncludeDirectories
- VC.Project.VCCLCompilerTool.AdditionalIncludeDirectories
- /I
- VC.Project.VCNMakeTool.IncludeSearchPath
helpviewer_keywords:
- /I compiler option [C++]
- Additional Include Directories compiler option
- I compiler option [C++]
- -I compiler option [C++]
- set include directories
- include directories, compiler option [C++]
ms.assetid: 3e9add2a-5ed8-4d15-ad79-5b411e313a49
ms.openlocfilehash: ad44abec28bbb87f91f449765a9ea2f30f2bffa8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191346"
---
# <a name="i-additional-include-directories"></a>/I (дополнительные каталоги включения)

Добавляет каталог в список каталогов для поиска включаемых файлов.

## <a name="syntax"></a>Синтаксис

> **/I**[]*Каталог*

### <a name="arguments"></a>Аргументы

*каталоги*<br/>
Каталог, добавляемый в список каталогов для поиска включаемых файлов.

## <a name="remarks"></a>Комментарии

Чтобы добавить несколько каталогов, используйте этот параметр более одного раза. Поиск в каталогах выполняется только до тех пор, пока не будет найден указанный включаемый файл.

Этот параметр можно использовать с параметром ([/x (игнорировать стандартные пути включения)](x-ignore-standard-include-paths.md)).

Компилятор выполняет поиск в каталогах в следующем порядке:

1. Если указывается с помощью [директивы #include](../../preprocessor/hash-include-directive-c-cpp.md) в форме двойных кавычек, она сначала выполняет поиск в локальных каталогах. Поиск начинается в том же каталоге, что и файл, содержащий инструкцию **#include** . Если не удается найти файл, он выполняет поиск в каталогах файлов, открытых в данный момент, в порядке, в котором они были открыты. Поиск начинается в каталоге родительского включаемого файла, а затем выполняется в каталогах всех включаемых файлов-прародителей.

1. Если параметр указан с помощью директивы **#include** в форме угловой скобки или при поиске в локальном каталоге произошел сбой, он ищет каталоги, указанные с помощью параметра **/i** , в том порядке, в котором компилятор обнаруживает их в командной строке.

1. Каталоги, указанные в переменной среды **include** .

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Перейдите на страницу свойств **Свойства конфигурации** > **C/C++**  > **Общие**.

1. Измените свойство **Дополнительные каталоги включаемых папок** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalIncludeDirectories%2A>.

## <a name="example"></a>Пример

Следующая команда ищет включаемые файлы, запрашиваемые функцией MAIN. c в следующем порядке: сначала, если он указан с помощью двойных кавычек, выполняется поиск локальных файлов. Затем поиск продолжится в каталоге \ИНКЛУДЕ, затем в каталоге \МИ\ИНКЛУДЕ и, наконец, в каталогах, назначенных переменной среды INCLUDE.

```
CL /I \INCLUDE /I\MY\INCLUDE MAIN.C
```

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
