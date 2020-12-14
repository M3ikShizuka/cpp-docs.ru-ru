---
description: Дополнительные сведения о:/stub ПРИЛАГАЕТ (имя файла заглушки MS-DOS)
title: /STUB (имя файла-заглушки MS-DOS)
ms.date: 11/04/2016
f1_keywords:
- /stub
- VC.Project.VCLinkerTool.DosStub
helpviewer_keywords:
- Win32 [C++], attaching MS-DOS stub program
- STUB linker option
- MS-DOS stub file name linker option
- /STUB linker option
- Windows API [C++], attaching MS-DOS stub program
- -STUB linker option
ms.assetid: 65221ffe-4f9a-4a14-ac69-3cfb79b40b5f
ms.openlocfilehash: 34f3cd71ce66cb6695a58707fd84de79f7a14b1d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230306"
---
# <a name="stub-ms-dos-stub-file-name"></a>/STUB (имя файла-заглушки MS-DOS)

```
/STUB:filename
```

## <a name="arguments"></a>Аргументы

*filename*<br/>
Приложение MS-DOS.

## <a name="remarks"></a>Комментарии

Параметр/STUB ПРИЛАГАЕТ подключает программу-заглушку MS-DOS к программе Win32.

Если файл выполняется в MS-DOS, вызывается программа-заглушка. Обычно отображается соответствующее сообщение. Однако любое допустимое приложение MS-DOS может быть программой-заглушкой.

Укажите *имя файла* программы-заглушки после двоеточия (:) в командной строке. Компоновщик проверяет *имя файла* и выдает сообщение об ошибке, если файл не является исполняемым. Программа должна быть файлом EXE; COM-файл недопустим для программы-заглушки.

Если этот параметр не используется, компоновщик присоединяет программу-заглушку по умолчанию, которая выдает следующее сообщение:

```
This program cannot be run in MS-DOS mode.
```

При создании драйвера виртуального устройства *имя файла* позволяет пользователю указать имя файла, содержащего структуру IMAGE_DOS_HEADER (определенную в Winnt. H) для использования в VXD, а не в заголовке по умолчанию.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр в поле **Дополнительные параметры** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
