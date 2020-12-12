---
description: Дополнительные сведения о:/FUNCTIONPADMIN (создание образа допускающего оперативное обновление)
title: /FUNCTIONPADMIN (создание образа, допускающего горячее обновление)
ms.date: 03/09/2018
f1_keywords:
- /functionpadmin
helpviewer_keywords:
- -FUNCTIONPADMIN linker option
- /FUNCTIONPADMIN linker option
ms.assetid: 25b02c13-1add-4fbd-add9-fcb30eb2cae7
ms.openlocfilehash: f86adb2001adacf1b6c8a03a90b7452505841c08
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192009"
---
# <a name="functionpadmin-create-hotpatchable-image"></a>/FUNCTIONPADMIN (создание образа, допускающего горячее обновление)

Подготавливает образ для горячего обновления.

## <a name="syntax"></a>Синтаксис

> **/FUNCTIONPADMIN**[**:**_Space_]

### <a name="arguments"></a>Аргументы

*модуль*<br/>
Объем заполнения, добавляемый в начало каждой функции в байтах. На платформе x86 это значение по умолчанию равно 5 байтам, а на x64 — по умолчанию — 6 байт. На других целевых объектах необходимо указать значение.

## <a name="remarks"></a>Комментарии

Чтобы компоновщик мог создать образ допускающего оперативное обновление, OBJ-файлы должны быть скомпилированы с помощью [/hotpatch (Create допускающего оперативное обновление Image)](hotpatch-create-hotpatchable-image.md).

При компиляции и связывании изображения с одним вызовом cl.exe **/hotpatch** подразумевает **/FUNCTIONPADMIN**.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Перейдите на страницу свойств **Свойства конфигурации** > **Компоновщик** > **Командная строка**.

1. Введите параметр **/FUNCTIONPADMIN** в поле **Дополнительные параметры**. Выберите **ОК** для сохранения внесенных изменений.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
