---
description: Дополнительные сведения о:/SWAPRUN (Загрузка выходных данных компоновщика в файл подкачки)
title: /SWAPRUN (загрузка выходных данных компоновщика в файл подкачки)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.SwapRunFromNet
- /swaprun
- VC.Project.VCLinkerTool.SwapRunFromCD
helpviewer_keywords:
- -SWAPRUN linker option
- files [C++], LINK
- LINK tool [C++], output
- linker [C++], copying output to swap file
- swap file for linker output
- output files, linker
- /SWAPRUN linker option
- SWAPRUN linker option
ms.assetid: 4a1e7f46-4399-4161-8dfc-d6a71beaf683
ms.openlocfilehash: f62d5e32432a2c738b7782c0fbf0cd4fd76a7f9a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230215"
---
# <a name="swaprun-load-linker-output-to-swap-file"></a>/SWAPRUN (загрузка выходных данных компоновщика в файл подкачки)

```
/SWAPRUN:{NET|CD}
```

## <a name="remarks"></a>Комментарии

Параметр/SWAPRUN указывает операционной системе сначала скопировать выходные данные компоновщика в файл подкачки, а затем запустить образ из него. Это функция Windows NT 4,0 (и более поздних версий).

Если указан параметр NET, операционная система сначала скопирует двоичный образ из сети в файл подкачки и загрузит его отсюда. Этот параметр полезен для запуска приложений по сети. Если указан параметр CD, операционная система скопирует образ на съемный диск в файл подкачки, а затем загрузит его.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **системы** .

1. Измените одно из следующих свойств:

   - **Переключение запуска с компакт-диска**

   - **Переключить запуск из сети**

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. описание свойств <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.SwapRunFromCD%2A> и <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.SwapRunFromNet%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
