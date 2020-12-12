---
description: Дополнительные сведения о перечислении ModuleType
title: ModuleType - перечисление
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::ModuleType
helpviewer_keywords:
- ModuleType enumeration
ms.assetid: 61a763af-a5a4-451d-8b40-815af507fcde
ms.openlocfilehash: 148f9594fd16a6c8a2af70ac0ff2ac03cd1f62e0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209377"
---
# <a name="moduletype-enumeration"></a>ModuleType - перечисление

Указывает, должен ли модуль поддерживать внутрипроцессный или внепроцессный сервер.

## <a name="syntax"></a>Синтаксис

```cpp
enum ModuleType;
```

## <a name="members"></a>Члены

### <a name="values"></a>Значения

|Имя|Описание|
|----------|-----------------|
|`InProc`|Внутрипроцессный сервер.|
|`OutOfProc`|Сервер вне процесса.|
|`DisableCaching`|Отключить механизм кэширования для модуля.|
|`InProcDisableCaching`|Сочетание `InProc` и `DisableCaching` .|
|`OutOfProcDisableCaching`|Сочетание `OutOfProc` и `DisableCaching` .|

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL](microsoft-wrl-namespace.md)
