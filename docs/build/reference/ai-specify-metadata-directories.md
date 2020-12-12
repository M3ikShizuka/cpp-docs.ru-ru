---
description: Дополнительные сведения о:/AI (указание каталогов метаданных)
title: /AI (указание каталогов метаданных)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLCompilerTool.AdditionalUsingDirectories
- VC.Project.VCNMakeTool.AssemblySearchPath
- /AI
- VC.Project.VCCLWCECompilerTool.AdditionalUsingDirectories
helpviewer_keywords:
- /AI compiler option [C++]
- AI compiler option [C++]
- -AI compiler option [C++]
ms.assetid: fb9c1846-504c-4a3b-bb39-c8696de32f6f
ms.openlocfilehash: e30711b1da2d41204bf56520d56dd5101f3168b2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179750"
---
# <a name="ai-specify-metadata-directories"></a>/AI (указание каталогов метаданных)

Указывает каталог, в котором компилятор будет производить поиск для разрешения ссылок, переданных в директиву `#using`.

## <a name="syntax"></a>Синтаксис

> _Каталог_ /AI

## <a name="arguments"></a>Аргументы

*каталоги*<br/>
Каталог или путь, по которому компилятор будет выполнять поиск.

## <a name="remarks"></a>Комментарии

Только один каталог может быть передан в вызов **/AI** . Укажите один параметр **/AI** для каждого пути, который должен искать компилятор. Например, чтобы добавить К:\прожект\мета и К:\коммон\мета в путь поиска компиляторов для `#using` директив, добавьте `/AI"C:\Project\Meta" /AI"C:\Common\Meta"` в командную строку компилятора или добавьте каждый каталог в свойство **дополнительное #using Directories** в Visual Studio.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Перейдите на страницу свойств **Свойства конфигурации** > **C/C++**  > **Общие**.

1. Измените свойство **Дополнительные каталоги #using** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalUsingDirectories%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
[Директива #using](../../preprocessor/hash-using-directive-cpp.md)
