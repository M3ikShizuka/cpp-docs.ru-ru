---
description: Дополнительные сведения о:/doc (обработка комментариев документации) (C/C++)
title: /doc (обработка комментариев документации) (C/C++)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLCompilerTool.GenerateXMLDocumentationFiles
- /doc
- VC.Project.VCCLCompilerTool.XMLDocumentationFileName
helpviewer_keywords:
- /doc compiler option [C++]
- comments, C++ code
- XML documentation, comments in source files
- -doc compiler option [C++]
ms.assetid: b54f7e2c-f28f-4f46-9ed6-0db09be2cc63
ms.openlocfilehash: ed811edff544c4b5b28baa67ed216fa09ea51092
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192880"
---
# <a name="doc-process-documentation-comments-cc"></a>/doc (обработка комментариев документации) (C/C++)

Заставляет компилятор обрабатывать комментарии документации в файлах исходного кода и создавать XDC для каждого файла исходного кода с комментариями к документации.

## <a name="syntax"></a>Синтаксис

> **/doc**[*имя*]

## <a name="arguments"></a>Аргументы

*name*<br/>
Имя XDC, который будет создан компилятором. Допустим только при передаче одного CPP-файла в компиляцию.

## <a name="remarks"></a>Комментарии

XDC-файлы обрабатываются в формате XML с xdcmake.exe. Дополнительные сведения см. в разделе [Справочник по xdcmake](xdcmake-reference.md).

Комментарии к документации можно добавить в файлы исходного кода. Дополнительные сведения см. в разделе [Рекомендуемые теги для комментариев документации](recommended-tags-for-documentation-comments-visual-cpp.md).

Чтобы использовать созданный XML-файл с IntelliSense, сделайте имя файла XML-файла таким же, как и сборка, которую требуется поддерживать, и помещает XML-файл в тот же каталог, что и сборка. При указании ссылки на сборку в проекте Visual Studio также обнаруживается XML-файл. Дополнительные сведения см. [в разделе Использование IntelliSense](/visualstudio/ide/using-intellisense) и [Указание комментариев XML-кода](/visualstudio/ide/supplying-xml-code-comments).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите   >  страницу свойств выходные файлы **C/C++** свойства конфигурации  >   .

1. Измените свойство **создать файлы XML-документации** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.GenerateXMLDocumentationFiles%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
