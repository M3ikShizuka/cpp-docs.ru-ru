---
description: Дополнительные сведения о:/NOLOGO (отключение загрузочного баннера) (компоновщик)
title: /NOLOGO (отмена вывода начального заголовка) (Компоновщик)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.SuppressStartupBanner
- /nologo
helpviewer_keywords:
- suppress startup banner linker option
- -NOLOGO linker option
- /NOLOGO linker option
- copyright message
- version numbers, preventing linker display
- banners, suppressing startup
- NOLOGO linker option
ms.assetid: 3b20dddd-eca6-4545-a331-9f70bf720197
ms.openlocfilehash: 48edea691e254f0754d29ab5ea4d8055221c4b69
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97196559"
---
# <a name="nologo-suppress-startup-banner-linker"></a>/NOLOGO (отмена вывода начального заголовка) (Компоновщик)

```
/NOLOGO
```

## <a name="remarks"></a>Комментарии

Параметр/NOLOGO не позволяет отобразить сообщение об авторских правах и номер версии.

Этот параметр также подавляет вывод командных файлов. Дополнительные сведения см. в разделе [компоновка командных файлов](linking.md).

По умолчанию эти сведения отправляются компоновщику в окно вывода. В командной строке он отправляется в стандартный вывод и может быть перенаправлен в файл.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Этот параметр следует использовать только из командной строки.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. Этот параметр компоновщика нельзя изменить программным способом.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
