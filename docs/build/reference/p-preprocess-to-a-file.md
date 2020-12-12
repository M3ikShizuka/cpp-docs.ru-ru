---
description: Дополнительные сведения о:/P (Предварительная обработка в файле)
title: /P (вывод результатов предварительной обработки в файл)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLCompilerTool.GeneratePreprocessedFile
- /p
- VC.Project.VCCLWCECompilerTool.GeneratePreprocessedFile
helpviewer_keywords:
- /P compiler option [C++]
- -P compiler option [C++]
- P compiler option [C++]
- output files, preprocessor
- preprocessing output files
ms.assetid: 123ee54f-8219-4a6f-9876-4227023d83fc
ms.openlocfilehash: 20bca03694c866baa0575445271fc4f587268096
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226198"
---
# <a name="p-preprocess-to-a-file"></a>/P (вывод результатов предварительной обработки в файл)

Предварительно обрабатывает исходные файлы C и C++ и записывает предварительно обработанные выходные данные в файл.

## <a name="syntax"></a>Синтаксис

```
/P
```

## <a name="remarks"></a>Remarks

Файл имеет то же базовое имя, что и исходный файл, и расширение. i. В процессе выполняются все директивы препроцессора, выполняются расширения макросов и удаляются комментарии. Чтобы сохранить комментарии в предварительно обработанном выводе, используйте параметр [/c (сохранять комментарии во время предварительной обработки)](c-preserve-comments-during-preprocessing.md) вместе с **/p**.

**/P** добавляет `#line` директивы в выходные данные в начале и в конце каждого включаемого файла и вокруг строк, удаленных директивами препроцессора для условной компиляции. Эти директивы перенумеруются строки предварительно обработанного файла. В результате ошибки, формируемые на последующих этапах обработки, ссылаются на номера строк исходного файла, а не на строки в предварительно обработанном файле. Чтобы подавить создание `#line` директив, используйте [/EP (Предварительная обработка в stdout без директив #line)](ep-preprocess-to-stdout-without-hash-line-directives.md) , а также **/p**.

Параметр **/p** подавляет компиляцию. Он не создает OBJ-файл, даже если используется команда [/FO (имя объектного файла)](fo-object-file-name.md). Необходимо повторно отправить предварительно обработанный файл для компиляции. Параметр **/p** также подавляет вывод выходных файлов из параметров **/FA**, **/FA** и **/FM** . Дополнительные сведения см. в разделе [/FA,/FA (файл листинга)](fa-fa-listing-file.md) и параметр [/FM (имя файла сопоставления)](fm-name-mapfile.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Щелкните страницу свойств **препроцессора** .

1. Измените свойство **создать предварительно обработанный файл** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.GeneratePreprocessedFile%2A>.

## <a name="example"></a>Пример

Следующая командная строка выполняет предварительную обработку `ADD.C` , сохраняет комментарии, добавляет `#line` директивы и записывает результат в файл `ADD.I` :

```
CL /P /C ADD.C
```

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
[/Fi (Предварительная обработка имени выходного файла)](fi-preprocess-output-file-name.md)
