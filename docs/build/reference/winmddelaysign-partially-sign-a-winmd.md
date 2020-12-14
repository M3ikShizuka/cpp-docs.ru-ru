---
description: Дополнительные сведения о:/WINMDDELAYSIGN (частичное подписание WinMD)
title: /WINMDDELAYSIGN (частично подпишите файл winmd)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.WINMDDelaySign
ms.assetid: 445cd602-62cb-400a-8e3a-4beb6572724d
ms.openlocfilehash: 801b172f52a9beb9d09617644b3096e460359724
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97259062"
---
# <a name="winmddelaysign-partially-sign-a-winmd"></a>/WINMDDELAYSIGN (частично подпишите файл winmd)

Включает частичную подпись файла метаданных среда выполнения Windows (WinMD), помещая открытый ключ в файл.

```
/WINMDDELAYSIGN[:NO]
```

## <a name="remarks"></a>Комментарии

Напоминает параметр компоновщика [/delaysign](delaysign-partially-sign-an-assembly.md) , применяемый к WinMD-файлу. Используйте **/WINMDDELAYSIGN** , если хотите поместить в WINMD-файл только открытый ключ. По умолчанию компоновщик работает так, как будто **/WINMDDELAYSIGN: NO не** указан. то есть он не подписывает WINMD-файл.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **Компоновщик** .

1. Выберите страницу свойств **метаданные Windows** .

1. В раскрывающемся списке « **Задержка метаданных Windows** » выберите нужный параметр.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
