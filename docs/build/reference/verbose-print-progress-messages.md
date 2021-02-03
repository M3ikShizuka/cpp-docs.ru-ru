---
description: Дополнительные сведения о:/VERBOSE (печать сообщений о ходе выполнения)
title: /VERBOSE (печать сообщений о ходе выполнения)
ms.date: 02/03/2021
f1_keywords:
- /verbose
- VC.Project.VCLinkerTool.ShowProgress
helpviewer_keywords:
- -VERBOSE linker option
- linking [C++], session progress information
- Print Progress Messages linker option
- linker [C++], output dependency information
- /VERBOSE linker option
- dependencies [C++], dependency information in linker output
- VERBOSE linker option
ms.openlocfilehash: d58a6cc8d75021c78f8161cf12957a77bb26483c
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522928"
---
# <a name="verbose-print-progress-messages"></a>`/VERBOSE` (Печать сообщений о ходе выполнения)

Выводит сообщения о ходе выполнения в процессе компоновки.

## <a name="syntax"></a>Синтаксис

> **`/VERBOSE`**\[**`:`**{**`CLR`**|**`ICF`**|**`INCR`**|**`LIB`**|**`REF`**|**`SAFESEH`**|**`UNUSEDDELAYLOAD`**|**`UNUSEDLIBS`**}\]

## <a name="remarks"></a>Примечания

Компоновщик отправляет сведения о ходе выполнения сеанса связывания в окно **вывода** . В командной строке сведения отправляются в стандартный вывод и могут быть перенаправлены в файл.

| Параметр | Описание |
| ------------ | ----------------- |
| **`/VERBOSE`** | Отображает подробные сведения о процессе компоновки. |
| **`/VERBOSE:CLR`** | Отображает сведения о действиях компоновщика, относящихся к объектам и метаданным, скомпилированным с помощью [`/clr`](clr-common-language-runtime-compilation.md) . |
| **`/VERBOSE:ICF`** | Отображает сведения о действии компоновщика, полученном в результате использования [`/OPT:ICF`](opt-optimizations.md) . |
| **`/VERBOSE:INCR`** | Отображает сведения о процессе инкрементной компоновки. |
| **`/VERBOSE:LIB`** | Отображает сообщения о ходе выполнения, указывающие только на те библиотеки, в которых выполняется поиск.<br/> Отображаемые сведения включают в себя процесс поиска библиотеки. В нем перечислены все библиотеки и имена объектов (с полными путями), символ, который разрешается из библиотеки, и список объектов, ссылающихся на этот символ. |
| **`/VERBOSE:REF`** | Отображает сведения о действии компоновщика, полученном в результате использования [`/OPT:REF`](opt-optimizations.md) . |
| **`/VERBOSE:SAFESEH`** | Отображает сведения о модулях, несовместимых с защищенной структурной обработкой исключений, если [`/SAFESEH`](safeseh-image-has-safe-exception-handlers.md) не указано. |
| **`/VERBOSE:UNUSEDDELAYLOAD`** | Отображает сведения о любых отложенно загруженных библиотеках DLL без символов, используемых при создании изображения. |
| **`/VERBOSE:UNUSEDLIBS`** | Отображает сведения о файлах библиотек, не используемых при создании образа. |

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Перейдите на страницу свойств **Свойства конфигурации** > **Компоновщик** > **Командная строка**.

1. Добавьте параметр в поле **Дополнительные параметры** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ShowProgress%2A>.

## <a name="see-also"></a>См. также

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
