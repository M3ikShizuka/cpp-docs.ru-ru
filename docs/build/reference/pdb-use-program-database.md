---
description: Дополнительные сведения:/PDB (использование базы данных программы)
title: /PDB (Использование базы данных программы)
ms.date: 11/04/2016
f1_keywords:
- /pdb
- VC.Project.VCLinkerTool.ProgramDatabaseFile
helpviewer_keywords:
- -PDB linker option
- /PDB linker option
- PDB linker option
- PDB files, creating
- .pdb files, creating
ms.assetid: d23db0ce-10cb-427a-bc60-d6b2a852723d
ms.openlocfilehash: 221d5d81dc3578e99751334b2e0a0a61aaaed356
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226107"
---
# <a name="pdb-use-program-database"></a>/PDB (Использование базы данных программы)

```
/PDB:filename
```

## <a name="arguments"></a>Аргументы

*filename*<br/>
Заданное пользователем имя для базы данных программы (PDB), создаваемой компоновщиком. Он заменяет имя по умолчанию.

## <a name="remarks"></a>Комментарии

По умолчанию при указании параметра [/Debug](debug-generate-debug-info.md) компоновщик создает базу данных программы (PDB), содержащую отладочную информацию. Имя файла по умолчанию для PDB имеет базовое имя программы и расширение PDB.

Используйте параметр/PDB:*filename* , чтобы указать имя PDB-файла. Если аргумент/DEBUG не указан, параметр/PDB игнорируется.

PDB-файл может иметь объем до 2 ГБ.

Дополнительные сведения см. [в разделе PDB-файлы в качестве входных файлов компоновщика](dot-pdb-files-as-linker-input.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Отладка** .

1. Измените свойство **создать файл базы данных программы** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ProgramDatabaseFile%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
