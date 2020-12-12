---
description: Дополнительные сведения:/NODEFAULTLIB (игнорирование библиотек)
title: Параметр /NODEFAULTLIB (пропуск библиотек)
ms.date: 03/26/2019
f1_keywords:
- VC.Project.VCLinkerTool.OVERWRITEAllDefaultLibraries
- VC.Project.VCLinkerTool.OVERWRITEDefaultLibraryNames
- /nodefaultlib
helpviewer_keywords:
- default libraries, removing
- -NODEFAULTLIB linker option
- libraries, ignore
- NODEFAULTLIB linker option
- /NODEFAULTLIB linker option
- ignore libraries linker option
ms.assetid: 7270b673-6711-468e-97a7-c2925ac2be6e
ms.openlocfilehash: 1443d7ac1e17d464baa829d8297234ae80f3b998
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97196715"
---
# <a name="nodefaultlib-ignore-libraries"></a>Параметр /NODEFAULTLIB (пропуск библиотек)

> **/NODEFAULTLIB**[__:__*Library*]

## <a name="arguments"></a>Аргументы

*Библиотечная*<br/>
Библиотека, которую должен игнорировать компоновщик при разрешении внешних ссылок.

## <a name="remarks"></a>Комментарии

Параметр/NODEFAULTLIB предписывает компоновщику удалить одну или несколько библиотек по умолчанию из списка библиотек, которые он ищет при разрешении внешних ссылок.

Чтобы создать OBJ-файл, который не содержит ссылок на библиотеки по умолчанию, используйте [параметр/Zl (не указывайте имя библиотеки по умолчанию)](zl-omit-default-library-name.md).

По умолчанию параметр/NODEFAULTLIB удаляет все стандартные библиотеки из списка библиотек, поиск которых выполняется при разрешении внешних ссылок. Необязательный параметр *библиотеки* позволяет удалить указанную библиотеку из списка библиотек, которые она ищет при разрешении внешних ссылок. Укажите один параметр/NODEFAULTLIB для каждой библиотеки, которую требуется исключить.

Компоновщик разрешает ссылки на внешние определения, сначала выполняя поиск в явно указанных библиотеках, затем в библиотеках по умолчанию, заданных параметром [параметр/DEFAULTLIB:](defaultlib-specify-default-library.md) , а затем в библиотеках по умолчанию с именами в OBJ-файлах.

/NODEFAULTLIB:*Библиотека* переопределяет параметр/DEFAULTLIB:*Library* , если в обоих случаях указано одно и то же имя *библиотеки* .

При использовании параметра/NODEFAULTLIB для создания программы без библиотеки времени выполнения C, возможно, потребуется также использовать [/entry](entry-entry-point-symbol.md) для указания функции точки входа в программе. Дополнительные сведения см. в разделе [Функции библиотеки CRT](../../c-runtime-library/crt-library-features.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите   >  страницу свойств входные свойства **компоновщика** свойств конфигурации  >   .

1. Выберите свойство **игнорировать все библиотеки по умолчанию** . Или укажите разделенный точками с запятой список библиотек, которые вы хотите игнорировать, в свойстве **игнорировать конкретные библиотеки по умолчанию** . На странице свойств **Командная строка** отображается результат изменений, внесенных в эти свойства.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. разделы <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.IgnoreDefaultLibraryNames%2A> и <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.IgnoreAllDefaultLibraries%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
