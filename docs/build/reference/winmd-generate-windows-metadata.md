---
description: Дополнительные сведения о:/WINMD (создание метаданных Windows)
title: /WINMD (создавать метаданные Windows)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.GenerateWindowsMetadata
ms.assetid: bcfb4901-411e-4c9e-9f78-23028b6e5fcc
ms.openlocfilehash: 7cf52a49716e6ec30a29c7e6a96fe7a078b4830c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97259088"
---
# <a name="winmd-generate-windows-metadata"></a>/WINMD (создавать метаданные Windows)

Включает создание файла метаданных среда выполнения Windows (WinMD).

> **/WinMD** \[ **:**{ \| **только** No}]

## <a name="arguments"></a>Аргументы

**/WINMD**<br/>
Значение по умолчанию для приложений универсальная платформа Windows. Компоновщик создает двоичный исполняемый файл и файл метаданных. winmd.

**/WINMD: НЕТ**<br/>
Компоновщик создает только двоичный исполняемый файл, но не WINMD-файл.

**/WINMD: ТОЛЬКО**<br/>
Компоновщик создает только WINMD-файл, но не двоичный исполняемый файл.

## <a name="remarks"></a>Комментарии

Параметр компоновщика **/WinMD** используется для приложений UWP и компонентов среды выполнения Windows для управления созданием файла метаданных Среда выполнения Windows (. winmd). WINMD-файл — это разновидность библиотеки DLL, которая содержит метаданные для типов среды выполнения Windows и, в случае компонентов среды выполнения, реализации этих типов. Метаданные следуют стандарту [ECMA-335](https://www.ecma-international.org/publications/standards/Ecma-335.htm) .

По умолчанию имя выходного файла имеет вид *бинаринаме*. winmd. Чтобы указать другое имя файла, используйте параметр [/WINMDFILE](winmdfile-specify-winmd-file.md) .

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте   >    >  страницу свойств **метаданные Windows** компоновщика свойства конфигурации.

1. В раскрывающемся списке **создать метаданные Windows** выберите нужный параметр.

## <a name="see-also"></a>См. также раздел

[Пошаговое руководство. Создание простого среда выполнения Windows компонента и вызов его из JavaScript](/windows/uwp/winrt-components/walkthrough-creating-a-simple-windows-runtime-component-and-calling-it-from-javascript)<br/>
[Введение в язык MIDL 3,0](/uwp/midl-3/intro)<br/>
[/WINMDFILE (указание WINMD-файла)](winmdfile-specify-winmd-file.md)<br/>
[/WINMDKEYFILE (указание файла ключа WinMD)](winmdkeyfile-specify-winmd-key-file.md)<br/>
[/WINMDKEYCONTAINER (указание контейнера ключей)](winmdkeycontainer-specify-key-container.md)<br/>
[/WINMDDELAYSIGN (частичное подписание WinMD)](winmddelaysign-partially-sign-a-winmd.md)<br/>
[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
