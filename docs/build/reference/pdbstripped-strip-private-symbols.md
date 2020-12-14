---
description: Дополнительные сведения о:/PDBSTRIPPED (чередование закрытых символов)
title: /PDBSTRIPPED (удалить закрытые символы)
ms.date: 11/04/2016
f1_keywords:
- /pdbstripped
- VC.Project.VCLinkerTool.StripPrivateSymbols
helpviewer_keywords:
- /PDBSTRIPPED linker option
- -PDBSTRIPPED linker option
- .pdb files, stripping private symbols
- PDB files, stripping private symbols
- PDBSTRIPPED linker option
ms.assetid: 9b9e0070-6a13-4142-8180-19c003fbbd55
ms.openlocfilehash: 27e70281ad12f4401ad6557ead9be11a38684472
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226042"
---
# <a name="pdbstripped-strip-private-symbols"></a>/PDBSTRIPPED (удалить закрытые символы)

```
/PDBSTRIPPED:pdb_file_name
```

## <a name="arguments"></a>Аргументы

*pdb_file_name*<br/>
Заданное пользователем имя для удаления базы данных программы (PDB), создаваемой компоновщиком.

## <a name="remarks"></a>Комментарии

Параметр/PDBSTRIPPED создает второй файл базы данных программы (PDB) при сборке образа программы с помощью любого из параметров компилятора или компоновщика, генерирующих PDB-файл ([/Debug](debug-generate-debug-info.md), [/Z7](z7-zi-zi-debug-information-format.md),/ZD или/Zi). Второй PDB-файл не содержит символов, которые нежелательно передавать клиентам. Второй PDB-файл будет содержать только следующие файлы:

- Открытые символы

- Список объектных файлов и частей исполняемого файла, в которые они участвуют

- Отладочная запись оптимизации указателя кадров (FPO), используемая для прохода по стеку

Очищенный PDB-файл не будет содержать следующие файлы:

- Сведения о типе

- Сведения о номере строки

- Файл для каждого объекта Информация CodeView символы, такие как для функций, локальных переменных и статических данных

Полный PDB-файл будет создан при использовании/ПДБСТРИППЕД.

Если не создать PDB-файл,/PDBSTRIPPED игнорируется.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Отладка** .

1. Измените свойство " **Удалить закрытые символы** ".

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.StripPrivateSymbols%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
