---
description: Дополнительные сведения:/FI (имя принудительно включаемого файла)
title: /FI (имя принудительно включаемого файла)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCNMakeTool.ForcedIncludes
- VC.Project.VCCLCompilerTool.ForcedIncludeFiles
- VC.Project.VCCLWCECompilerTool.ForcedIncludeFiles
helpviewer_keywords:
- FI compiler option [C++]
- -FI compiler option [C++]
- /FI compiler option [C++]
- preprocess header file compiler option [C++]
ms.assetid: 07e79577-8152-4df9-a64c-aae08c603397
ms.openlocfilehash: 614a06511df1b407adc39bb8ec567a9674ffb3cc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200654"
---
# <a name="fi-name-forced-include-file"></a>/FI (имя принудительно включаемого файла)

Приводит к обработке препроцессором указанного файла заголовка.

## <a name="syntax"></a>Синтаксис

```
/FI[ ]pathname
```

## <a name="remarks"></a>Remarks

Этот параметр имеет тот же результат, что и при указании файла с двойными кавычками в `#include` директиве в первой строке каждого исходного файла, указанного в командной строке, в переменной среды CL или в командном файле. При использовании нескольких параметров **/Fi** файлы включаются в том порядке, в котором они обрабатываются компилятором CL.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Перейдите на страницу свойств **Дополнительно** .

1. Измените свойство **принудительно включаемого файла** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ForcedIncludeFiles%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры OUTPUT-File (/F)](output-file-f-options.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
[Указание пути](specifying-the-pathname.md)
