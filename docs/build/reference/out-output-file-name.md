---
description: Дополнительные сведения о:/OUT (имя выходного файла)
title: /OUT (имя выходного файла)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.OutputFile
- /out
helpviewer_keywords:
- output files, name linker option
- -OUT linker option
- OUT linker option
- /OUT C++ linker option
- linker [C++], output files
ms.assetid: 976210a4-e51f-4cfb-af5e-c16344455834
ms.openlocfilehash: 1773b4b2dd340bc105495c1b05211c018548976f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226406"
---
# <a name="out-output-file-name"></a>/OUT (имя выходного файла)

```
/OUT:filename
```

## <a name="arguments"></a>Аргументы

*filename*<br/>
Заданное пользователем имя выходного файла. Он заменяет имя по умолчанию.

## <a name="remarks"></a>Комментарии

Параметр/OUT переопределяет имя и расположение программы, создаваемой компоновщиком по умолчанию.

По умолчанию компоновщик формирует имя файла, используя базовое имя первого указанного OBJ-файла и соответствующее расширение (exe или DLL).

Этот параметр является базовым именем по умолчанию для файла. сопоставления или библиотеки импорта. Дополнительные сведения см. в разделе [Generate сопоставления](map-generate-mapfile.md) (/Map) и [/ImpLib](implib-name-import-library.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Общие** .

1. Измените свойство **выходного файла** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.OutputFile%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
