---
description: Дополнительные сведения о:/IMPLIB (имя библиотеки импорта)
title: /IMPLIB (именование библиотеки импорта)
ms.date: 11/04/2016
f1_keywords:
- /implib
- VC.Project.VCLinkerTool.ImportLIbrary
helpviewer_keywords:
- IMPLIB linker option
- /IMPLIB linker option
- -IMPLIB linker option
- import libraries, overriding default name
ms.assetid: fe8f71ab-7055-41b5-8ef8-2b97cfa4a432
ms.openlocfilehash: 2a5ea590368d1bc3abbecf38845e97a99a0d1f96
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191320"
---
# <a name="implib-name-import-library"></a>/IMPLIB (именование библиотеки импорта)

> /IMPLIB:*имя файла*

## <a name="parameters"></a>Параметры

*filename*<br/>
Заданное пользователем имя библиотеки импорта. Он заменяет имя по умолчанию.

## <a name="remarks"></a>Комментарии

Параметр/IMPLIB переопределяет имя по умолчанию для библиотеки импорта, создаваемой LINK при сборке программы, содержащей EXPORTS. Имя по умолчанию формируется на основе базового имени основного выходного файла и расширения LIB. Программа содержит экспорты, если указано одно или несколько из следующих данных:

- Ключевое слово [__declspec (dllexport)](../../cpp/dllexport-dllimport.md) в исходном коде

- [Экспортирует](exports.md) инструкцию в DEF-файле

- Спецификация [/Export](export-exports-a-function.md) в команде LINK

LINK игнорирует/IMPLIB, если библиотека импорта не создается. Если экспорты не указаны, LINK не создает библиотеку импорта. Если в сборке используется файл экспорта, то LINK предполагает, что библиотека импорта уже существует и не создает ее. Сведения о библиотеках импорта и файлах экспорта см. в [справочнике по lib](lib-reference.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Дополнительно** .

1. Измените свойство **Библиотека импорта** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ImportLibrary%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
