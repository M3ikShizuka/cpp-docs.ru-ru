---
description: Подробнее о:/FIXED (фиксированный базовый адрес)
title: /FIXED (фиксированный базовый адрес)
ms.date: 11/04/2016
f1_keywords:
- /fixed
- VC.Project.VCLinkerTool.FixedBaseAddress
helpviewer_keywords:
- preferred base address for loading program
- /FIXED linker option
- -FIXED linker option
- FIXED linker option
ms.assetid: 929bba5e-b7d8-40ed-943e-056aa3710fc5
ms.openlocfilehash: 08b781b7fbeaf43d6c7e0e82da7bf8319cf77953
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192061"
---
# <a name="fixed-fixed-base-address"></a>/FIXED (фиксированный базовый адрес)

```
/FIXED[:NO]
```

## <a name="remarks"></a>Комментарии

Указывает операционной системе загрузить программу только по предпочтительному базовому адресу. Если предпочтительный базовый адрес недоступен, операционная система не загружает файл. Дополнительные сведения см. в разделе [/base (базовый адрес)](base-base-address.md).

/FIXED: NO является параметром по умолчанию для библиотеки DLL, а параметр/FIXED является значением по умолчанию для любого другого типа проекта.

Если задан параметр /FIXED, то программа LINK не создает в программе секцию перемещения. Во время выполнения, если операционная система не может загрузить программу по указанному адресу, она выдает сообщение об ошибке и не загружает программу.

Для создания раздела перемещения в программе укажите параметр/FIXED: NO.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **Компоновщик** .

1. Выберите страницу свойств **Командная строка** .

1. Введите имя параметра и параметр в поле **Дополнительные параметры** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
