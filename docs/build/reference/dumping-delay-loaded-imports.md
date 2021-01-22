---
description: 'Дополнительные сведения: дампы импорта с отложенной загрузкой'
title: Импорт с отложенной загрузкой импорта
ms.date: 01/19/2021
helpviewer_keywords:
- delay-loaded imports, dumping
- imports (delay-loaded)
- delay-loaded imports
ms.openlocfilehash: 6a0fec0b10bc29ea919195302334a25f71de0abd
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98666918"
---
# <a name="dump-delay-loaded-imports"></a>Импорт с отложенной загрузкой импорта

Операции импорта с отложенной загрузкой можно выгрузить с помощью [`dumpbin /imports`](imports-dumpbin.md) . Эти импорты отображаются с немного отличающимися сведениями, чем стандартные операции импорта. Они разделяются на отдельные разделы `/imports` списка и явно помечены как импортированные с отложенной загрузкой. Если на изображении есть сведения о выгрузке, это отмечается. Если сведения о привязке присутствуют, то метка времени и даты для целевой библиотеки DLL указывается вместе с связанными адресами импорта.

## <a name="see-also"></a>См. также раздел

[Поддержка компоновщика для библиотек DLL с отложенной загрузкой](linker-support-for-delay-loaded-dlls.md)
