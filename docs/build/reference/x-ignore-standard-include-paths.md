---
description: 'Дополнительные сведения: `/X` (игнорировать стандартные пути включаемых файлов)'
title: /X (игнорирование стандартных путей включения)
ms.date: 01/21/2021
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
ms.openlocfilehash: 97d19027c41df7db9103c1c21d2f2d7b8d398e7e
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98712808"
---
# <a name="x-ignore-standard-include-paths"></a>`/X` (Игнорировать стандартные пути включаемых файлов)

Не разрешает компилятору выполнять поиск включаемых файлов в каталогах, указанных в `PATH` `INCLUDE` переменных среды и.

## <a name="syntax"></a>Синтаксис

> **`/X`**

## <a name="remarks"></a>Примечания

Этот параметр можно использовать с параметром [ `/I` (дополнительные каталоги включения)](i-additional-include-directories.md) , чтобы указать альтернативный путь к стандартным включаемым файлам.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите   >  страницу свойств препроцессора свойства конфигурации **C/C++**  >   .

1. Измените свойство " **игнорировать стандартные включаемые пути** ".

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.IgnoreStandardIncludePath%2A>.

## <a name="example"></a>Пример

В следующей команде **`/X`** сообщает компилятору, что следует игнорировать расположения, указанные `PATH` `INCLUDE` переменными среды и, и **`/I`** указывает каталог для поиска включаемых файлов:

```cmd
CL /X /I \ALT\INCLUDE MAIN.C
```

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис командной строки компилятора MSVC](compiler-command-line-syntax.md)
