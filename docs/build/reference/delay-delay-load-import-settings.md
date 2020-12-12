---
description: Дополнительные сведения о:/DELAY (параметры отложенной загрузки импорта)
title: /DELAY (параметры отложенной загрузки импортов)
ms.date: 11/04/2016
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
ms.assetid: 9334b332-cc58-4dae-b10f-a4c75972d50c
ms.openlocfilehash: f06a47280d563c138e184fdbdcdf033da705ce60
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201525"
---
# <a name="delay-delay-load-import-settings"></a>/DELAY (параметры отложенной загрузки импортов)

```
/DELAY:UNLOAD
/DELAY:NOBIND
```

## <a name="remarks"></a>Комментарии

Параметр/DELAY управляет [отложенной загрузкой](linker-support-for-delay-loaded-dlls.md) библиотек DLL:

- Квалификатор UNLOAD предписывает вспомогательной функции отложенной загрузки поддерживать явную выгрузку DLL. Таблица адресов импорта (IAT) восстанавливается в своем первоначальном виде; это приводит к тому, что указатели IAT становятся недействительными и перезаписываются.

   Если не выбрать параметр Выгрузить, любой вызов [фунлоадделайлоадеддлл](explicitly-unloading-a-delay-loaded-dll.md) завершится ошибкой.

- Квалификатор NOBIND предписывает компоновщику не включать связываемую таблицу IAT в окончательный образ. По умолчанию задано создание связываемой таблицы IAT для библиотек DLL, загружаемых с задержкой. Полученный в результате образ не может быть статически привязан. (Изображения с возможностью привязки ИАТС могут быть статически привязаны перед выполнением.) См. [/BIND](bind.md).

   Если библиотека DLL привязана, вспомогательная функция будет пытаться использовать привязанные сведения вместо вызова [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) на каждом из импортируемых импортов. Если метка времени или предпочтительный адрес не соответствуют таковым в загружаемой библиотеке DLL, то вспомогательная функция будет предполагать, что привязанная таблица IAT устарела, и продолжать обработку так, будто привязанной таблицы IAT не существует.

   Применение квалификатора NOBIND приведет к увеличению образа программы, но зато может уменьшить время загрузки библиотеки DLL. Если привязка библиотеки DLL не предполагалась, то NOBIND предотвратит создание привязанной таблицы IAT.

Чтобы указать библиотеки DLL для задержки загрузки, используйте параметр [параметр/DELAYLOAD](delayload-delay-load-import.md) .

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Дополнительные сведения см. [в разделе Установка компилятора C++ и свойств сборки в Visual Studio](../working-with-project-properties.md).

1. Разверните узел **Свойства конфигурации**, **Компоновщик** и выберите **Дополнительно**.

1. Измените свойство **DLL с отложенной загрузкой** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.DelayLoadDLLs%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
