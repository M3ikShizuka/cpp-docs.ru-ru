---
description: Дополнительные сведения о:/VERBOSE (печать сообщений о ходе выполнения)
title: /VERBOSE (печать сообщений о ходе выполнения)
ms.date: 06/13/2019
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
ms.assetid: 9c347d98-4c37-4724-a39e-0983934693ab
ms.openlocfilehash: 9d1a22a1b05f42a707b2449fbb114ba06db85ff5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97176422"
---
# <a name="verbose-print-progress-messages"></a>/VERBOSE (печать сообщений о ходе выполнения)

Выводит сообщения о ходе выполнения в процессе компоновки.

## <a name="syntax"></a>Синтаксис

> **/Verbose** \[ **:**{**Среда CLR** | **ICF** | **INCR** | **lib** | **ref** |  | **унуседделайлоад** | **унуседлибс**}\]

## <a name="remarks"></a>Комментарии

Компоновщик отправляет сведения о ходе выполнения сеанса связывания в окно **вывода** . В командной строке сведения отправляются в стандартный вывод и могут быть перенаправлены в файл.

| Параметр | Описание |
| ------------ | ----------------- |
| /VERBOSE | Отображает подробные сведения о процессе компоновки. |
| /VERBOSE: СРЕДА CLR | Отображает сведения о действиях компоновщика, относящихся к объектам и метаданным, скомпилированным с помощью [/CLR](clr-common-language-runtime-compilation.md). |
| /VERBOSE: ICF | Отображает сведения о действиях компоновщика, полученных в результате использования параметра [/OPT: ICF](opt-optimizations.md). |
| /VERBOSE: INCR | Отображает сведения о процессе инкрементной компоновки. |
| /VERBOSE: LIB | Отображает сообщения о ходе выполнения, указывающие только на те библиотеки, в которых выполняется поиск.<br/> Отображаемые сведения включают в себя процесс поиска библиотеки. В нем перечислены все библиотеки и имена объектов (с полными путями), символ, который разрешается из библиотеки, и список объектов, ссылающихся на этот символ. |
| /VERBOSE: REF | Отображает сведения о действиях компоновщика, полученных в результате использования параметра [/OPT: REF](opt-optimizations.md). |
| /VERBOSE: SAFESEH | Отображает сведения о модулях, несовместимых с защищенной структурной обработкой исключений, если параметр [/SAFESEH](safeseh-image-has-safe-exception-handlers.md) не указан. |
| /VERBOSE: УНУСЕДДЕЛАЙЛОАД | Отображает сведения о любых отложенно загруженных библиотеках DLL без символов, используемых при создании изображения. |
| /VERBOSE: УНУСЕДЛИБС | Отображает сведения о файлах библиотек, не используемых при создании образа. |

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Перейдите на страницу свойств **Свойства конфигурации** > **Компоновщик** > **Командная строка**.

1. Добавьте параметр в поле **Дополнительные параметры** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ShowProgress%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
