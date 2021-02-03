---
description: Дополнительные сведения о:/DELAY (параметры отложенной загрузки импорта)
title: /DELAY (параметры импорта отложенной загрузки)
ms.date: 01/28/2021
f1_keywords:
- /delay
- VC.Project.VCLinkerTool.DelayNoBind
- VC.Project.VCLinkerTool.SupportUnloadOfDelayLoadedDLL
- VC.Project.VCLinkerTool.DelayUnload
helpviewer_keywords:
- delayed loading of DLLs, /DELAY option
- DELAY linker option
- /DELAY linker option
- -DELAY linker option
ms.openlocfilehash: 0dd6aaaffd378afe4ca7d75180da869b2748d639
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522200"
---
# <a name="delay-delay-load-import-settings"></a>`/DELAY` (Параметры отложенной загрузки импорта)

Параметры компоновщика для управления отложенной загрузкой библиотек DLL во время выполнения.

## <a name="syntax"></a>Синтаксис

> **`/DELAY:UNLOAD`**\
> **`/DELAY:NOBIND`**

## <a name="remarks"></a>Примечания

**`/DELAY`** Параметр управляет [отложенной загрузкой](linker-support-for-delay-loaded-dlls.md) библиотек DLL:

- **`/DELAY:UNLOAD`** Квалификатор указывает вспомогательной функции отложенной загрузки поддерживать явную выгрузку библиотеки DLL. Таблица адресов импорта (IAT) восстанавливается в своем первоначальном виде; это приводит к тому, что указатели IAT становятся недействительными и перезаписываются.

   Если не выбрать **`/DELAY:UNLOAD`** , вызов [`__FUnloadDelayLoadedDLL`](linker-support-for-delay-loaded-dlls.md#explicitly-unload-a-delay-loaded-dll) завершится ошибкой.

- **`/DELAY:NOBIND`** Квалификатор указывает компоновщику не включать связываемую IAT в окончательный образ. По умолчанию задано создание связываемой таблицы IAT для библиотек DLL, загружаемых с задержкой. Полученный образ не может быть статически привязан. (Изображения с возможностью привязки ИАТС могут быть статически привязаны перед выполнением.) Дополнительные сведения см. в разделе [`/BIND`](bind.md) .

   Если библиотека DLL привязана, вспомогательная функция пытается использовать привязанные сведения вместо вызова [`GetProcAddress`](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) на каждом из импортируемых ссылок. Если либо отметка времени, либо предпочтительный адрес не совпадают с теми, которые находятся в загруженной библиотеке DLL, то вспомогательная функция предполагает, что связанная таблица IAT устарела. Она будет продолжаться, как если бы связанная таблица IAT не существовала.

   **`/DELAY:NOBIND`** приводит к увеличению размера образа программы, но может ускорить загрузку библиотеки DLL. Если вы никогда не планируете привязывать библиотеку DLL, не попытается **`/DELAY:NOBIND`** создать привязанную IAT.

Чтобы указать библиотеки DLL для задержки загрузки, используйте [`/DELAYLOAD`](delayload-delay-load-import.md) параметр.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Дополнительные сведения см. [в разделе Установка компилятора C++ и свойств сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите вкладку **Свойства конфигурации**  >  **компоновщика**  >  **Дополнительные** свойства.

1. Измените свойство **DLL с отложенной загрузкой** . Выберите **ОК** для сохранения внесенных изменений.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.DelayLoadDLLs%2A>.

## <a name="see-also"></a>См. также

[Справочник по компоновщику КОМПИЛЯТОРОМ MSVC](linking.md)\
[Параметры компоновщика MSVC](linker-options.md)
