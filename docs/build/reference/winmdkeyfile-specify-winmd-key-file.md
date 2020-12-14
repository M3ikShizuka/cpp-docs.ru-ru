---
description: Дополнительные сведения о:/WINMDKEYFILE (указание файла ключа WinMD)
title: /WINMDKEYFILE (укажите файл ключей winmd)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.WINMDKeyFile
ms.assetid: 65d88fdc-fff9-49ea-8cfc-b2f408741734
ms.openlocfilehash: 0e7b23de62613f51c3824b107e55180bb54780d1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97258906"
---
# <a name="winmdkeyfile-specify-winmd-key-file"></a>/WINMDKEYFILE (укажите файл ключей winmd)

Задает ключ или пару ключей для подписи файла метаданных среда выполнения Windows (WinMD).

```
/WINMDKEYFILE:filename
```

## <a name="remarks"></a>Комментарии

Напоминает параметр компоновщика [/keyfile](keyfile-specify-key-or-key-pair-to-sign-an-assembly.md) , применяемый к WinMD-файлу.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **Компоновщик** .

1. Выберите страницу свойств **метаданные Windows** .

1. В поле **файл ключа метаданных Windows** введите расположение файла.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
