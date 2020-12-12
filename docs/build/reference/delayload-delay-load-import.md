---
description: 'Дополнительные сведения о: параметр/DELAYLOAD (отложенная загрузка импорта)'
title: /DELAYLOAD (загрузка импорта с задержкой)
ms.date: 11/04/2016
f1_keywords:
- /delayload
- VC.Project.VCLinkerTool.DelayLoadDLLS
helpviewer_keywords:
- DELAYLOAD linker option
- -DELAYLOAD linker option
- /DELAYLOAD linker option
- delayed loading of DLLs, /DELAYLOAD option
ms.assetid: 39ea0f1e-5c01-450f-9c75-2d9761ff9b28
ms.openlocfilehash: 9f6a91a102b66a16896d51b960d44273a7935d79
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201499"
---
# <a name="delayload-delay-load-import"></a>/DELAYLOAD (загрузка импорта с задержкой)

> **Параметр/DELAYLOAD:**_dllname_

## <a name="parameters"></a>Параметры

*dllname*<br/>
Имя DLL-библиотеки, загрузку которой нужно задержать.

## <a name="remarks"></a>Комментарии

При использовании параметра /DELAYLOAD DLL-библиотека, указанная с помощью `dllname`, загружается только при первом вызове функции этой DLL-библиотеки программой. Дополнительные сведения см. в разделе [Поддержка компоновщика для Delay-Loadedных библиотек DLL](linker-support-for-delay-loaded-dlls.md). Можно использовать этот параметр сколько угодно раз, указывая сколько угодно DLL-библиотек. При компоновке программы нужно использовать Delayimp.lib. Также можно использовать собственную вспомогательную функцию загрузки с задержкой.

Параметр [/delay](delay-delay-load-import-settings.md) задает параметры привязки и загрузки для каждой библиотеки DLL с отложенной загрузкой.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. В папке **Компоновщик** выберите страницу свойств **входные данные** .

1. Измените свойство **DLL с отложенной загрузкой** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.DelayLoadDLLs%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
