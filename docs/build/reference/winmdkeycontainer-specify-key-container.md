---
description: Дополнительные сведения о:/WINMDKEYCONTAINER (указание контейнера ключей)
title: /WINMDKEYCONTAINER (указать контейнер ключей)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.WINMDKEYCONTAINER
ms.assetid: c2fc44dc-7cb5-42b9-897f-1b124928f2f7
ms.openlocfilehash: 94b203c56b7724c2b2569ba22039da38c4501985
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97258997"
---
# <a name="winmdkeycontainer-specify-key-container"></a>/WINMDKEYCONTAINER (указать контейнер ключей)

Указывает контейнер ключей для подписи файла метаданных Windows (WinMD).

```
/WINMDKEYCONTAINER:name
```

## <a name="remarks"></a>Комментарии

Напоминает параметр компоновщика [/keycontainer](keycontainer-specify-a-key-container-to-sign-an-assembly.md) , применяемый к файлу (. winmd).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **Компоновщик** .

1. Выберите страницу свойств **метаданные Windows** .

1. В поле **контейнер ключа метаданных Windows** введите расположение.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
