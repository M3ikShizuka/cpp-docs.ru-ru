---
description: Дополнительные сведения о:/Y-(игнорировать параметры предкомпилированного заголовка)
title: /Y- (пропуск параметров предкомпилированного заголовка)
ms.date: 11/04/2016
f1_keywords:
- /y-
helpviewer_keywords:
- Y- compiler option [C++]
- -Y- compiler option [C++]
- /Y- compiler option [C++]
ms.assetid: cfaecb36-58db-46b8-b04d-cca6072b1b7a
ms.openlocfilehash: b3d1eb6d404e0463ee547c1905f792b485bf65f6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97260843"
---
# <a name="y--ignore-precompiled-header-options"></a>/Y- (пропуск параметров предкомпилированного заголовка)

Приводит к `/Y` игнорированию всех остальных параметров компилятора (и не может быть переопределено).

## <a name="syntax"></a>Синтаксис

```
/Y-
```

## <a name="remarks"></a>Remarks

Дополнительные сведения о предкомпилированных заголовках см. в следующих статьях:

- [/Y (предварительно скомпилированные заголовки)](y-precompiled-headers.md)

- [Файлы предкомпилированных заголовков](../creating-precompiled-header-files.md)

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
