---
description: Дополнительные сведения о:/FC (полный путь к файлу исходного кода в диагностике)
title: /FC (полный путь к файлу исходного кода в папке Diagnostics)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLCompilerTool.UseFullPaths
- /FC
helpviewer_keywords:
- /FC compiler option [C++]
- -FC compiler option [C++]
ms.assetid: 1f11414e-cb42-421b-be68-9d369aab036b
ms.openlocfilehash: 01d1148a32179a7c605a19dc7f2856b7697ae6fb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200680"
---
# <a name="fc-full-path-of-source-code-file-in-diagnostics"></a>/FC (полный путь к файлу исходного кода в папке Diagnostics)

Приводит к тому, что компилятор отображает полный путь к файлам исходного кода, переданным компилятору в ходе диагностики.

## <a name="syntax"></a>Синтаксис

> /FC

## <a name="remarks"></a>Комментарии

Рассмотрим следующий пример кода:

```cpp
// compiler_option_FC.cpp
int main( ) {
   int i   // C2143
}
```

Без **/FC** текст диагностического текста будет выглядеть примерно так:

- compiler_option_FC. cpp (5): Error C2143: синтаксическая ошибка: отсутствует ";" перед "}"

При использовании **/FC** текст диагностического текста будет выглядеть примерно так:

- к:\тест\ compiler_option_fc. cpp (5): ошибка C2143: синтаксическая ошибка: отсутствует ";" перед "}"

**/FC** также требуется, если требуется просмотреть полный путь к имени файла при использовании макроса &#95;&#95;File&#95;&#95; . Дополнительные сведения о &#95;&#95;&#95;&#95; файлов см. в разделе [предопределенные макросы](../../preprocessor/predefined-macros.md) .

Параметр **/FC** подразумевается **/Zi**. Дополнительные сведения о параметре **/Zi** см. в разделе [/Z7,/Zi,/Zi (формат отладочной информации)](z7-zi-zi-debug-information-format.md).

**/FC** выводит полные пути в нижнем регистре.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств свойства **конфигурации**  >  **C/C++**  >  **Дополнительно** .

1. Измените свойство **использовать полные пути** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.UseFullPaths%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
