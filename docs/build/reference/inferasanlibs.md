---
description: Дополнительные сведения о параметре компоновщика/ИНФЕРАСАНЛИБС (use выводимые библиотеки очистки)
title: /ИНФЕРАСАНЛИБС (использование выводимых библиотек очистки)
ms.date: 03/01/2021
f1_keywords:
- /INFERASANLIBS
- /INFERASANLIBS:NO
helpviewer_keywords:
- /INFERASANLIBS [C++]
- address sanitizer [C++] linker option
ms.openlocfilehash: 82337b5b77bab2a9066427662f3fd0956684c636
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471106"
---
# <a name="inferasanlibs-use-inferred-sanitizer-libs"></a>`/INFERASANLIBS` (Использование выводимых библиотек очистки)

Используйте **`/INFERASANLIBS`** параметр компоновщика, чтобы включить или отключить связывание с библиотеками аддресссанитизер по умолчанию. Начиная с Visual Studio 2019 16,9, поддерживается только [аддресссанитизер](../../sanitizers/asan.md).

## <a name="syntax"></a>Синтаксис

> **`/INFERASANLIBS`**\[**`:NO`**]

## <a name="remarks"></a>Комментарии

**`/INFERASANLIBS`** Параметр компоновщика включает библиотеки [аддресссанитизер](../../sanitizers/asan.md) по умолчанию. Этот параметр по умолчанию включен.

**`/INFERASANLIBS`** **`/INFERASANLIBS:NO`** Параметры компоновщика и предлагают поддержку для опытных пользователей. Дополнительные сведения см. в разделе [Справочник по сборке и языку аддресссанитизер](../../sanitizers/asan-building.md).

Этот **`/INFERASANLIBS`** параметр доступен начиная с Visual Studio 2019 версии 16,9.

### <a name="to-set-the-inferasanlibs-linker-option-in-the-visual-studio-development-environment"></a>Установка **`/INFERASANLIBS`** параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **страницы свойств** проекта.

1. Перейдите на страницу свойств **Свойства конфигурации** > **Компоновщик** > **Командная строка**.

1. Измените свойство **Дополнительные параметры** . Чтобы включить библиотеки по умолчанию, введите **/инферасанлибс** в поле ввода. Чтобы отключить библиотеки по умолчанию, введите **/инферасанлибс: No** .

1. Нажмите кнопку **ОК** или **Применить** , чтобы сохранить изменения.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также

[Справочник по компоновщику КОМПИЛЯТОРОМ MSVC](linking.md)\
[Параметры компоновщика КОМПИЛЯТОРОМ MSVC](linker-options.md)\
[`/fsanitize` (Включить чистку)](./fsanitize.md)\
[Обзор Аддресссанитизер](../../sanitizers/asan.md)\
[Известные проблемы Аддресссанитизер](../../sanitizers/asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](../../sanitizers/asan-building.md)
