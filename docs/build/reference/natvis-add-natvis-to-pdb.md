---
description: Дополнительные сведения о:/НАТВИС (Добавление Natvis в PDB)
title: /NATVIS (добавление файла NATVIS в файл PDB)
ms.date: 08/10/2017
f1_keywords:
- /natvis
helpviewer_keywords:
- NATVIS linker option
- /NATVIS linker option
- -NATVIS linker option
- Add Natvis file to PDB
ms.assetid: 8747fc0c-701a-4796-bb4d-818ab4465cca
ms.openlocfilehash: 7703915591a59a558c8580dd64b9be22d281d784
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190527"
---
# <a name="natvis-add-natvis-to-pdb"></a>/NATVIS (добавление файла NATVIS в файл PDB)

> /НАТВИС:*имя файла*

## <a name="parameters"></a>Параметры

*filename*<br/>
Natvis-файл для добавления в PDB-файл. Он внедряет визуализацию отладчика в файл Natvis в PDB.

## <a name="remarks"></a>Комментарии

Параметр/НАТВИС внедряет визуализации отладчика, определенные в файле Natvis-файла, в PDB *-файл,* созданный LINK. Это позволяет отладчику отображать визуализации независимо от natvis – файла. Можно использовать несколько параметров/НАТВИС для внедрения нескольких Natvis-файлов в созданный PDB-файл.

LINK игнорирует/НАТВИС, если PDB-файл не создается с помощью параметра [/Debug](debug-generate-debug-info.md) . Сведения о создании и использовании natvis файлов см. [в разделе Создание пользовательских представлений собственных объектов в отладчике Visual Studio](/visualstudio/debugger/create-custom-views-of-native-objects).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств **Командная строка** в папке **Компоновщик** .

1. Добавьте параметр/НАТВИС в текстовое поле **Дополнительные параметры** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- Этот параметр не имеет программного эквивалента.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
