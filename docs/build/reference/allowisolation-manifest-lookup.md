---
description: Дополнительные сведения о:/ALLOWISOLATION (поиск манифеста)
title: /ALLOWISOLATION (поиск манифеста)
ms.date: 11/04/2016
f1_keywords:
- /ALLOWISOLATION
- VC.Project.VCLinkerTool.AllowIsolation
helpviewer_keywords:
- -ALLOWISOLATION linker option
- /ALLOWISOLATION linker option
ms.assetid: 6d41851e-b3c1-4bdf-beaa-031773089d6f
ms.openlocfilehash: 659c908e4de910941ca71c9f40814608df19c6d4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97187225"
---
# <a name="allowisolation-manifest-lookup"></a>/ALLOWISOLATION (поиск манифеста)

Задает поведение нахождения файлов манифеста.

## <a name="syntax"></a>Синтаксис

```
/ALLOWISOLATION[:NO]
```

## <a name="remarks"></a>Remarks

**/ALLOWISOLATION: нет** означает, что библиотеки DLL загружены, как если бы манифеста не было, и заставляет компоновщик установить `IMAGE_DLLCHARACTERISTICS_NO_ISOLATION` бит в поле необязательного заголовка `DllCharacteristics` .

**/ALLOWISOLATION** заставляет операционную систему выполнять поиск и загрузку манифеста.

По умолчанию используется **/ALLOWISOLATION** .

Если для исполняемого объекта отключена изоляция, загрузчик Windows не будет пытаться найти манифест приложения для только что созданного процесса. Новый процесс не будет иметь контекста активации по умолчанию, даже если манифест находится внутри исполняемого файла или находится в том же каталоге, что и исполняемый файл с именем <em>Executable-Name</em>**. exe. manifest**.

Дополнительные сведения см. в разделе [Справочник по файлам манифеста](/windows/win32/SbsCs/manifest-files-reference).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте   >    >  страницу свойств **файл манифеста** компоновщика свойств конфигурации.

1. Измените значение свойства **Разрешить изоляцию** .

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
