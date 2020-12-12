---
description: Дополнительные сведения о:/C (сохранение комментариев во время предварительной обработки)
title: /C (сохранять комментарии во время предварительной обработки)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLCompilerTool.KeepComments
- VC.Project.VCCLWCECompilerTool.KeepComments
helpviewer_keywords:
- comments, not stripping during preprocessing
- preserve comments during preprocessing
- -c compiler option [C++]
- c compiler option [C++]
- /c compiler option [C++]
ms.assetid: 944567ca-16bc-4728-befe-d414a7787f26
ms.openlocfilehash: 2cf5bf562db78dcb6c570d7313b56ad4a9fc5adb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179360"
---
# <a name="c-preserve-comments-during-preprocessing"></a>/C (сохранять комментарии во время предварительной обработки)

Сохраняет комментарии на этапе предварительной обработки.

## <a name="syntax"></a>Синтаксис

```
/C
```

## <a name="remarks"></a>Remarks

Для этого параметра компилятора требуется параметр **/e**, **/p** или **/EP** .

В следующем образце кода отображается комментарий к исходному коду.

```cpp
// C_compiler_option.cpp
// compile with: /E /C /c
int i;   // a variable
```

В этом примере будут получены следующие выходные данные.

```
#line 1 "C_compiler_option.cpp"
int i;   // a variable
```

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Щелкните страницу свойств **препроцессора** .

1. Измените свойство " **оставить комментарии** ".

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.KeepComments%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
[/E (Предварительная обработка до stdout)](e-preprocess-to-stdout.md)<br/>
[/P (Предварительная обработка в файле)](p-preprocess-to-a-file.md)<br/>
[/EP (Предварительная обработка в stdout без директив #line)](ep-preprocess-to-stdout-without-hash-line-directives.md)
