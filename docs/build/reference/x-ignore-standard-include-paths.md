---
description: 'Дополнительные сведения: `/X` (игнорировать стандартные пути включаемых файлов)'
title: /X (игнорирование стандартных путей включения)
ms.date: 07/31/2020
f1_keywords:
- /x
- VC.Project.VCCLCompilerTool.OVERWRITEStandardIncludePath
- VC.Project.VCCLWCECompilerTool.OVERWRITEStandardIncludePath
- VC.Project.VCCLCompilerTool.IgnoreStandardIncludePath
helpviewer_keywords:
- /X compiler option [C++]
- include files, ignore standard path
- -X compiler option [C++]
- include directories, ignore standard
- X compiler option
- Ignore Standard Include Paths compiler option
ms.assetid: 16bdf2cc-c8dc-46e4-bdcc-f3caeba5e1ef
ms.openlocfilehash: 69936b80893de2c45622ec9973a218a94e8029a4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97261012"
---
# <a name="x-ignore-standard-include-paths"></a>`/X` (Игнорировать стандартные пути включаемых файлов)

Предотвращает Поиск включаемых файлов в каталогах, указанных в переменных среды PATH и INCLUDE, компилятором.

## <a name="syntax"></a>Синтаксис

> **`/X`**

## <a name="remarks"></a>Remarks

Этот параметр можно использовать с параметром [ `/I` (дополнительные каталоги включения)](i-additional-include-directories.md) , чтобы указать альтернативный путь к стандартным включаемым файлам.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите   >  страницу свойств препроцессора свойства конфигурации **C/C++**  >   .

1. Измените свойство " **игнорировать стандартные включаемые пути** ".

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.IgnoreStandardIncludePath%2A>.

## <a name="example"></a>Пример

В следующей команде **`/X`** сообщает компилятору, что следует игнорировать расположения, указанные в переменных среды PATH и include, а **`/I`** также указать каталог для поиска включаемых файлов:

```cmd
CL /X /I \ALT\INCLUDE MAIN.C
```

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис командной строки компилятора MSVC](compiler-command-line-syntax.md)
