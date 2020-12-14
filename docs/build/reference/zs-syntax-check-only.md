---
description: Дополнительные сведения о:/ZS (только проверка синтаксиса)
title: /Zs (Только синтаксическая проверка)
ms.date: 11/04/2016
f1_keywords:
- /zs
helpviewer_keywords:
- -Zs compiler option [C++]
- Syntax Check Only compiler option
- Zs compiler option
- /Zs compiler option [C++]
ms.assetid: b4b41e6a-3f41-4d09-9cb6-fde5aa2cfecf
ms.openlocfilehash: a4f5e2227104003a637db1d921fd959ea0a11ad7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97224300"
---
# <a name="zs-syntax-check-only"></a>/Zs (Только синтаксическая проверка)

Указывает компилятору проверять только синтаксис исходных файлов в командной строке.

## <a name="syntax"></a>Синтаксис

```
/Zs
```

## <a name="remarks"></a>Remarks

При использовании этого параметра выходные файлы не создаются, а сообщения об ошибках записываются в стандартный вывод.

Параметр **/ZS** обеспечивает быстрый способ поиска и исправления синтаксических ошибок перед компиляцией и связыванием исходного файла.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
