---
description: Дополнительные сведения:/FM (имя файла сопоставления)
title: Параметр /Fm (имя файла сопоставления)
ms.date: 11/04/2016
f1_keywords:
- /fm
helpviewer_keywords:
- -Fm compiler option [C++]
- mapfiles [C++], creating linker
- files [C++], creating map
- Fm compiler option [C++]
- /Fm compiler option [C++]
ms.assetid: 8154448a-93a7-4546-8e4c-5c44d0aff45d
ms.openlocfilehash: 5c86a18ae9880a499997bcac2d8411859753d858
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200485"
---
# <a name="fm-name-mapfile"></a>Параметр /Fm (имя файла сопоставления)

Указывает компоновщику создать файл сопоставления, содержащий список сегментов в том порядке, в котором они отображаются в соответствующем exe-файле или DLL.

## <a name="syntax"></a>Синтаксис

```
/Fmpathname
```

## <a name="remarks"></a>Remarks

По умолчанию файл сопоставления получает базовое имя соответствующего исходного файла C или C++ с помощью. Расширение MAP.

Указание параметра **/FM** имеет тот же результат, что и если был указан параметр компоновщика [/Map (Generate сопоставления)](map-generate-mapfile.md) .

Если указать параметр [/c (компилировать без компоновки)](c-compile-without-linking.md) , чтобы подавить компоновку, параметр **/FM** не будет действовать.

Глобальные символы в соавторе обычно имеют один или несколько символов подчеркивания в начале, так как компилятор добавляет в имена переменных символ подчеркивания в начале. Многие глобальные символы, отображаемые в параметре сопоставления, используются внутренне компилятором и стандартными библиотеками.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры OUTPUT-File (/F)](output-file-f-options.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
[Указание пути](specifying-the-pathname.md)
