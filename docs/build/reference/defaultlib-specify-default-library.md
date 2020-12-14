---
description: 'Дополнительные сведения о: параметр/DEFAULTLIB (указание библиотеки по умолчанию)'
title: /DEFAULTLIB (определение библиотеки по умолчанию)
ms.date: 05/29/2018
f1_keywords:
- VC.Project.VCLinkerTool.DefaultLibraries
- /defaultlib
helpviewer_keywords:
- -DEFAULTLIB linker option
- DEFAULTLIB linker option
- /DEFAULTLIB linker option
- libraries, adding to list of
ms.assetid: 6af7ff49-c170-4a13-97e2-2b9ae2de20c9
ms.openlocfilehash: 9abaf158ed01b3e0a04d29c55d213c8749462c43
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201694"
---
# <a name="defaultlib-specify-default-library"></a>/DEFAULTLIB (определение библиотеки по умолчанию)

Укажите библиотеку по умолчанию для поиска, чтобы разрешить внешние ссылки.

## <a name="syntax"></a>Синтаксис

> **Параметр/DEFAULTLIB**:_Библиотека_

### <a name="arguments"></a>Аргументы

*Библиотечная*<br/>
Имя библиотеки для поиска при разрешении внешних ссылок.

## <a name="remarks"></a>Комментарии

Параметр **параметр/DEFAULTLIB** добавляет одну *библиотеку* в список библиотек, которые ссылаются на поиск при разрешении ссылок. Библиотека, указанная с помощью **параметр/DEFAULTLIB** , ищется после явно указанных библиотек в командной строке и перед библиотеками по умолчанию с именами в OBJ-файлах.

При использовании без аргументов параметр [/NODEFAULTLIB (игнорировать все библиотеки по умолчанию)](nodefaultlib-ignore-libraries.md) переопределяет все параметры **параметр/DEFAULTLIB**:*Library* . Параметр **/NODEFAULTLIB**:*Library* переопределяет *библиотеку* **параметр/DEFAULTLIB**:, если в обоих случаях указано одно и то же имя *библиотеки* .

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Окна свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойств сборки в Visual Studio](../working-with-project-properties.md).

1. Перейдите на страницу свойств **Свойства конфигурации** > **Компоновщик** > **Командная строка**.

1. В окне **Дополнительные параметры** введите параметр **параметр/DEFAULTLIB**:*Library* для каждой библиотеки, в которой будет производиться поиск. Выберите **ОК** для сохранения внесенных изменений.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

- [Справочник по компоновщику MSVC](linking.md)
- [Параметры компоновщика MSVC](linker-options.md)
