---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4222'
title: Предупреждение средств компоновщика LNK4222
ms.date: 11/04/2016
f1_keywords:
- LNK4222
helpviewer_keywords:
- LNK4222
ms.assetid: b7bb1794-41fb-4c83-b9b0-59c0d786a7da
ms.openlocfilehash: 215dd04339b783d558b05140bb7dd08c5936d5e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222611"
---
# <a name="linker-tools-warning-lnk4222"></a>Предупреждение средств компоновщика LNK4222

экспортируемому символу "Symbol" не следует присваивать порядковый номер

Следующие символы не должны экспортироваться по порядковому номеру:

- `DllCanUnloadNow`

- `DllGetClassObject`

- `DllGetClassFactoryFromClassString`

- `DllInstall`

- `DllRegisterServer`

- `DllRegisterServerEx`

- `DllUnregisterServer`

Эти функции всегда находятся по имени с помощью `GetProcAddress` . Компоновщик предупреждает об этом типе экспорта, так как это может привести к увеличению изображения. Это может произойти, если диапазон порядковых номеров экспорта велик с относительно небольшими экспортами. например следующие.

```
EXPORTS
   DllGetClassObject   @1
   MyOtherAPI      @100
```

потребует 100 слотов в таблице адресов экспорта с 98 (2-99) просто заполнения. С другой стороны

```
EXPORTS
   DllGetClassObject
   MyOtherAPI      @100
```

потребуется два слота. (Имейте в виду, что можно также экспортировать с параметром компоновщика [/Export](../../build/reference/export-exports-a-function.md) .)
