---
description: Дополнительные сведения см. в разделе/bigobj (увеличение числа разделов в). OBJ-файл)
title: /bigobj (Увеличение количества разделов в OBJ-файле)
ms.date: 03/26/2019
f1_keywords:
- /bigobj
helpviewer_keywords:
- -bigobj compiler option [C++]
- /bigobj compiler option [C++]
- bigobj compiler option [C++]
ms.assetid: ba94d602-4015-4a8d-86ec-49241ab74c12
ms.openlocfilehash: 4e820211ec46ad2a2d125552f95fb8a82c6f57ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97182701"
---
# <a name="bigobj-increase-number-of-sections-in-obj-file"></a>/bigobj (Увеличение количества разделов в OBJ-файле)

**/bigobj** увеличивает количество разделов, которые может содержать объектный файл.

## <a name="syntax"></a>Синтаксис

> **/bigobj**

## <a name="remarks"></a>Комментарии

По умолчанию объектный файл может содержать до 65 279 (почти 2 ^ 16) адресных секций. Это ограничение действует независимо от того, какая целевая платформа указана. **/bigobj** увеличивает емкость адреса до 4 294 967 296 (2 ^ 32).

Большинство модулей никогда не создают OBJ-файл, содержащий более 65 279 разделов. Однако для кода, созданного машинным кодом, или кода, который использует библиотеки шаблонов, могут потребоваться OBJ-файлы, в которых могут содержаться дополнительные разделы. параметр **/bigobj** включен по умолчанию в проектах универсальная платформа Windows (UWP), поскольку созданный компьютером код XAML включает большое количество заголовков. Если отключить этот параметр для проекта приложения UWP, код может вызвать ошибку компилятора C1128.

Сведения о формате объектного файла PE-COFF см. в разделе [Формат PE](/windows/win32/debug/pe-format) в документации по Windows.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств **Свойства конфигурации**  >  **C/C++**  >  **Командная строка** .

1. В поле **Дополнительные параметры** введите параметр компилятора **/bigobj** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
