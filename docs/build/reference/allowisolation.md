---
description: Дополнительные сведения о:/ALLOWISOLATION
title: /ALLOWISOLATION
ms.date: 11/04/2016
f1_keywords:
- /ALLOWISOLATION_EDITBIN
helpviewer_keywords:
- -ALLOWISOLATION editbin option
- /ALLOWISOLATION editbin option
- ALLOWISOLATION editbin option
ms.assetid: 91430344-f64f-491a-a5a5-7ea3b21cbe68
ms.openlocfilehash: 7d935bc122b5f32bb8f1193feae58b5fc61e7faa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179594"
---
# <a name="allowisolation"></a>/ALLOWISOLATION

Задает поведение нахождения файлов манифеста.

## <a name="syntax"></a>Синтаксис

```

/ALLOWISOLATION[:NO]
```

## <a name="remarks"></a>Remarks

**/ALLOWISOLATION** заставляет операционную систему выполнять поиск и загрузку манифеста.

По умолчанию используется **/ALLOWISOLATION** .

**/ALLOWISOLATION: нет** означает, что исполняемые файлы загружаются, как если бы манифеста не было, и заставляет [ссылку EDITBIN](editbin-reference.md) задать `IMAGE_DLLCHARACTERISTICS_NO_ISOLATION` бит в поле необязательного заголовка `DllCharacteristics` .

Если изоляция для исполняемого файла отключена, загрузчик Windows не пытается найти манифест приложения для нового процесса. Новый процесс не имеет контекста активации по умолчанию, даже если существует манифест в самом исполняемом файле или если имеется манифест с именем *Executable*. exe. manifest.

## <a name="see-also"></a>См. также раздел

[Параметры EDITBIN](editbin-options.md)<br/>
[/ALLOWISOLATION (поиск манифеста)](allowisolation-manifest-lookup.md)<br/>
[Справочник по файлам манифеста](/windows/win32/SbsCs/manifest-files-reference)
