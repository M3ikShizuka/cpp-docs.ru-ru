---
description: Дополнительные сведения о параметре компилятора/фсанитизе (Enable очистки)
title: /фсанитизе (включение очистки)
ms.date: 02/24/2021
f1_keywords:
- /fsanitize
- -fsanitize
- /fsanitize=address
- /fsanitize-address-use-after-return
- -fsanitize-address-use-after-return
- /fno-sanitize-address-vcasan-lib
- -fno-sanitize-address-vcasan-lib
helpviewer_keywords:
- /fsanitize [C++]
- -fsanitize=address [C++]
- address sanitizer compiler option [C++]
- /fsanitize-address-use-after-return
- /fno-sanitize-address-vcasan-lib
ms.openlocfilehash: 820d39e54db29a5e06d119cbefc8a1980447e8cc
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471102"
---
# <a name="fsanitize-enable-sanitizers"></a>`/fsanitize` (Включить чистку)

Используйте **`/fsanitize`** параметры компилятора, чтобы включить средства очистки. Начиная с Visual Studio 2019 16,9, поддерживается только [аддресссанитизер](../../sanitizers/asan.md).

## <a name="syntax"></a>Синтаксис

> **`/fsanitize=address`**\
> **`/fsanitize-address-use-after-return`**\
> **`/fno-sanitize-address-vcasan-lib`**

## <a name="remarks"></a>Remarks

**`/fsanitize=address`** Параметр компилятора включает [аддресссанитизер](../../sanitizers/asan.md), мощную технологию компилятора и среды выполнения для облегчения [поиска ошибок](../../sanitizers/asan.md#error-types).

**`/fsanitize-address-use-after-return`** **`/fno-sanitize-address-vcasan-lib`** Параметры компилятора и [ `/INFERASANLIBS` (использование выводимых библиотек](./inferasanlibs.md) средства очистки) и **`/INFERASANLIBS:NO`** Параметры компоновщика предлагают поддержку для опытных пользователей. Дополнительные сведения см. в разделе [Справочник по сборке и языку аддресссанитизер](../../sanitizers/asan-building.md).

**`/fsanitize`** Параметры доступны начиная с Visual Studio 2019 версии 16,9.

### <a name="to-set-the-fsanitizeaddress-compiler-option-in-the-visual-studio-development-environment"></a>Установка **`/fsanitize=address`** параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **страницы свойств** проекта.

1. Перейдите на страницу свойств **Свойства конфигурации** > **C/C++**  > **Общие**.

1. Измените свойство " **включить очистку адреса** ". Чтобы включить его, выберите **Да (/фсанитизе = адрес)**.

1. Нажмите кнопку **ОК** или **Применить** , чтобы сохранить изменения.

### <a name="to-set-the-advanced-compiler-options"></a>Задание дополнительных параметров компилятора

1. Откройте диалоговое окно **страницы свойств** проекта.

1. Выберите страницу свойств **Свойства конфигурации**  >  **C/C++**  >  **Командная строка** .

1. Измените свойство **Дополнительные параметры** , чтобы задать **/фсанитизе-Аддресс-усе-Афтер-ретурн** или **/ФНО-санитизе-Аддресс-вкасан-либ**.

1. Нажмите кнопку **ОК** или **Применить** , чтобы сохранить изменения.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также

[Параметры компилятора КОМПИЛЯТОРОМ MSVC](compiler-options.md)\
[Синтаксис командной строки компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)\
[`/INFERASANLIBS` (Использование выводимых библиотек очистки)](./inferasanlibs.md)\
[Обзор Аддресссанитизер](../../sanitizers/asan.md)\
[Известные проблемы Аддресссанитизер](../../sanitizers/asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](../../sanitizers/asan-building.md)
