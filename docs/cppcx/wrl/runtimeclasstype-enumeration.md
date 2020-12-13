---
description: Дополнительные сведения о перечислении RuntimeClassType
title: RuntimeClassType - перечисление
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::RuntimeClassType
helpviewer_keywords:
- RuntimeClassType enumeration
ms.assetid: d380712d-672e-4ea9-b7c5-cf9fa7dbb770
ms.openlocfilehash: 10055d79148124e886c4da50e40ffdb7d3d0fec0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97135282"
---
# <a name="runtimeclasstype-enumeration"></a>RuntimeClassType - перечисление

Указывает поддерживаемый тип экземпляра [RuntimeClass](runtimeclass-class.md) .

## <a name="syntax"></a>Синтаксис

```cpp
enum RuntimeClassType;
```

## <a name="members"></a>Члены

### <a name="values"></a>Значения

|Имя|Описание|
|----------|-----------------|
|`ClassicCom`|Классический класс среды выполнения COM.|
|`Delegate`|Эквивалент `ClassicCom`.|
|`InhibitFtmBase`|Отключает `FtmBase` поддержку `__WRL_CONFIGURATION_LEGACY__` , пока не определена.|
|`InhibitWeakReference`|Отключает поддержку слабых ссылок.|
|`WinRt`|Класс среда выполнения Windows.|
|`WinRtClassicComMix`|Комбинация `WinRt` и `ClassicCom`.|

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL](microsoft-wrl-namespace.md)
