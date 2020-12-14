---
description: Дополнительные сведения о:/WINMDFILE (указание WINMD-файла)
title: /WINMDFILE (укажите файл winmd)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.GenerateWindowsMetadataFile
ms.assetid: 062b41b3-14d6-432c-a361-fdb66e918931
ms.openlocfilehash: fd10768c494bbedfbe650e0f0e3e72e8a062cdc1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97259023"
---
# <a name="winmdfile-specify-winmd-file"></a>/WINMDFILE (укажите файл winmd)

Задает имя выходного файла метаданных среда выполнения Windows (. winmd), создаваемого параметром компоновщика [/WinMD](winmd-generate-windows-metadata.md) .

```
/WINMDFILE:filename
```

## <a name="remarks"></a>Комментарии

Используйте значение, указанное в, `filename` чтобы переопределить имя файла. winmd ( `binaryname` . winmd) по умолчанию. Обратите внимание, что ". winmd" не добавляется в `filename` .  Если в командной строке **/WINMDFILE** указано несколько значений, то приоритет имеет последняя из них.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **Компоновщик** .

1. Выберите страницу свойств **метаданные Windows** .

1. В поле **файл метаданных Windows** введите расположение файла.

## <a name="see-also"></a>См. также раздел

[/WINMD (создание метаданных Windows)](winmd-generate-windows-metadata.md)<br/>
[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
