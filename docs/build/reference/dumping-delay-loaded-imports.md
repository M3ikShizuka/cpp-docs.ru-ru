---
description: 'Дополнительные сведения о: дампы Delay-Loadedных импортов'
title: Сохранение отложенно загружаемых импортированных элементов
ms.date: 11/04/2016
helpviewer_keywords:
- delay-loaded imports, dumping
- imports (delay-loaded)
- delay-loaded imports
ms.assetid: f766acf4-9df8-4b85-8cf6-0be3ffc4c124
ms.openlocfilehash: c57ff6bb4a3dce16b4cb1eb85fdffff4ef272396
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201083"
---
# <a name="dumping-delay-loaded-imports"></a>Сохранение отложенно загружаемых импортированных элементов

Импорт с отложенной загрузкой может быть выгружен с помощью [dumpbin/imports](imports-dumpbin.md) и отображаться с немного отличающимися сведениями, чем стандартные операции импорта. Они разделяются в отдельный раздел дампа/Imports и явно помечены как импортированные с отложенной загрузкой. Если в образе имеются сведения о выгрузке, то это отмечается. Если имеются сведения о привязке, отметка даты и времени целевой DLL-библиотеки указывается вместе с связанными адресами импорта.

## <a name="see-also"></a>См. также раздел

[Поддержка компоновщика для Delay-Loadedных библиотек DLL](linker-support-for-delay-loaded-dlls.md)
