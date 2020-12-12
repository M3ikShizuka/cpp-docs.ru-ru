---
description: Дополнительные сведения о:/ALIGN (выравнивание разделов)
title: /ALIGN (выравнивание разделов)
ms.date: 12/29/2017
f1_keywords:
- VC.Project.VCLinkerTool.Alignment
- /align
helpviewer_keywords:
- sections, specifying alignment
- ALIGN linker option
- /ALIGN linker option
- -ALIGN linker option
- section alignment
- sections
ms.openlocfilehash: d8a9af473252a2eff8957c5d2b4c54c7f7c862aa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97187264"
---
# <a name="align-section-alignment"></a>/ALIGN (выравнивание разделов)

## <a name="syntax"></a>Синтаксис

> **/Align**[**:**_число_]

### <a name="arguments"></a>Аргументы

*number*<br/>
Значение выравнивания в байтах.

## <a name="remarks"></a>Комментарии

Параметр **/align** задает выравнивание каждого раздела в линейном адресном пространстве программы. Аргумент *Number* находится в байтах и должен быть степенью числа 2. Значение по умолчанию — 4 КБ (4096). Компоновщик выдает предупреждение, если при выравнивании создается недопустимое изображение.

Если вы не пишете приложение, например драйвер устройства, не нужно изменять выравнивание.

Можно изменить выравнивание определенного раздела с помощью параметра «выравнивание» для параметра [/section](section-specify-section-attributes.md) .

Указанное значение выравнивания не может быть меньше, чем максимальное выравнивание раздела.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Перейдите на   >    >  страницу свойства **командной строки** компоновщика свойств конфигурации.

1. Введите параметр в поле **Дополнительные параметры** . Нажмите кнопку **ОК** или **Применить** , чтобы применить изменение.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
