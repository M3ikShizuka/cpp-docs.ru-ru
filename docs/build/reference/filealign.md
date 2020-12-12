---
description: Подробнее о:/FILEALIGN (выровняйте разделы в файлах)
title: /FILEALIGN (выравнивание разделов в файлах)
ms.date: 10/23/2017
f1_keywords:
- /filealign
helpviewer_keywords:
- linker align sections
- /FILEALIGN linker option
- -FILEALIGN linker option
- FILEALIGN linker option
ms.assetid: c1017a35-8d71-4ad9-934b-a3e3ea037fa0
ms.openlocfilehash: a67cf682c8fe55b80b2253864e08919e08242f74
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192166"
---
# <a name="filealign-align-sections-in-files"></a>/FILEALIGN (выравнивание разделов в файлах)

Параметр компоновщика **/filealign** позволяет указать выравнивание разделов, записанных в выходной файл, в виде кратного указанного размера.

## <a name="syntax"></a>Синтаксис

> __/Filealign:__*Размер*

### <a name="parameters"></a>Параметры

*size*<br/>
Размер выравнивания раздела в байтах, который должен быть степенью числа 2.

## <a name="remarks"></a>Примечания

Параметр **/filealign** заставляет компоновщик выстроить каждый раздел выходного файла на границе, кратной значению *размера* . По умолчанию компоновщик не использует фиксированный размер выравнивания.

Параметр **/filealign** можно использовать, чтобы повысить эффективность использования диска или ускорить загрузку страниц с диска. Размер раздела меньшего размера может быть полезен для приложений, работающих на небольших устройствах, или для меньших версий загрузок. Выравнивание разделов на диске не влияет на выравнивание в памяти.

Используйте [DUMPBIN](dumpbin-reference.md) для просмотра информации о разделах выходного файла.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств **Командная строка** в папке **Компоновщик** .

1. Введите имя параметра **/filealign:** и размер в поле **Дополнительные параметры** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
