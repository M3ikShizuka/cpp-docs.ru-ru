---
description: Дополнительные сведения о:/MAP (создание файла сопоставления)
title: /MAP (создание файла сопоставления)
ms.date: 11/04/2016
f1_keywords:
- /map
- VC.Project.VCLinkerTool.MapFileName
- VC.Project.VCLinkerTool.GenerateMapFile
helpviewer_keywords:
- mapfiles, creating linker
- generate mapfile linker option
- mapfile linker option
- mapfiles, information about program being linked
- MAP linker option
- -MAP linker option
- mapfiles, specifying file name
- /MAP linker option
ms.assetid: 9ccce53d-4e36-43da-87b0-7603ddfdea63
ms.openlocfilehash: 28e3823099b4893dcf344a0b1aae99577d850821
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97176435"
---
# <a name="map-generate-mapfile"></a>/MAP (создание файла сопоставления)

```
/MAP[:filename]
```

## <a name="arguments"></a>Аргументы

*filename*<br/>
Заданное пользователем имя файла сопоставления. Он заменяет имя по умолчанию.

## <a name="remarks"></a>Комментарии

Параметр/MAP указывает компоновщику создать параметр сопоставления.

По умолчанию компоновщик присваивает файлу сопоставления базовое имя программы и расширение Map. Дополнительное имя *файла* позволяет переопределить имя файла сопоставления по умолчанию.

Файл сопоставления является текстовым файлом, который содержит следующие сведения о связанной программе:

- Имя модуля, являющееся базовым именем файла

- Метка времени из заголовка файла программы (не из файловой системы)

- Список групп в программе с начальным адресом каждой группы (как *раздел*:*смещение*), длиной, именем группы и классом.

- Список общедоступных символов с каждым адресом (в виде *раздела*:*offset*), именем символа, неструктурированным адресом и OBJ-файлом, в котором определен символ.

- Точка входа (как *раздел*:*смещение*)

Параметр [/MapInfo](mapinfo-include-information-in-mapfile.md) задает дополнительные сведения для включения в параметр сопоставления.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Отладка** .

1. Измените свойство **создать файл отображения** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. разделы <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.GenerateMapFile%2A> и <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.MapFileName%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
