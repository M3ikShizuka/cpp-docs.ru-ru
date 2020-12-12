---
description: Дополнительные сведения о:/ZW (компиляция среда выполнения Windows)
title: /ZW (компиляция среды выполнения Windows)
ms.date: 04/08/2019
f1_keywords:
- VC.Project.VCCLCompilerTool.CompileAsWinRT
- /zw
helpviewer_keywords:
- /ZW
- -ZW compiler option
- /ZW compiler option
- -ZW
- Windows Runtime compiler option
ms.assetid: 0fe362b0-9526-498b-96e0-00d7a965a248
ms.openlocfilehash: b2c39cdfb3f1d22d12c8d07b1e844c550a7a0e3a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97273921"
---
# <a name="zw-windows-runtime-compilation"></a>/ZW (компиляция среды выполнения Windows)

Компилирует исходный код для поддержки расширений Microsoft C++ Component Extensions C++/CX для создания приложений универсальная платформа Windows (UWP).

При использовании **/ZW** для компиляции всегда указывайте параметр **/EHsc** .

## <a name="syntax"></a>Синтаксис

```cpp
/ZW /EHsc
/ZW:nostdlib /EHsc
```

## <a name="arguments"></a>Аргументы

**nostdlib**<br/>
Указывает на то, что Platform.winmd, Windows.Foundation.winmd и другие файлы метаданных Windows по умолчанию (WINMD) не включаются в компиляцию автоматически. Вместо этого для явного указания файлов метаданных Windows необходимо использовать параметр компилятора [/Fu (имя принудительно #using файл)](fu-name-forced-hash-using-file.md) .

## <a name="remarks"></a>Комментарии

При указании параметра **/ZW** компилятор поддерживает следующие функции:

- Необходимые файлы метаданных, пространства имен, типы данных и функции, которые требуются приложению для выполнения в среда выполнения Windows.

- Автоматический подсчет ссылок на объекты среда выполнения Windows и автоматическая отмена удаления объекта, когда его счетчик ссылок становится равным нулю.

Поскольку добавочный компоновщик не поддерживает метаданные Windows, включенные в OBJ-файлы с помощью параметра **/ZW** , устаревший параметр [/GM (включение минимального перестроения)](gm-enable-minimal-rebuild.md) несовместим с **/ZW**.

Дополнительные сведения см. в разделе [Справочник по языку Visual C++](../../cppcx/visual-c-language-reference-c-cx.md).

## <a name="requirements"></a>Требования

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
