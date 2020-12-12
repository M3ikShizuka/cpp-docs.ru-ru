---
description: 'Дополнительные сведения о: Катлаутосреадмодуле Class'
title: Класс Катлаутосреадмодуле
ms.date: 11/04/2016
f1_keywords:
- CAtlAutoThreadModule
- atlbase/ATL::CAtlAutoThreadModule
helpviewer_keywords:
- CAtlAutoThreadModule class
ms.assetid: 3be834aa-55ef-403e-94ae-41979691b15f
ms.openlocfilehash: d1742488cca84dccfa53753bec40f9081d77f67d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97165060"
---
# <a name="catlautothreadmodule-class"></a>Класс Катлаутосреадмодуле

Этот класс реализует COM-сервер модели подразделения в пуле потоков.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
class CAtlAutoThreadModule : public CAtlAutoThreadModuleT<CAtlAutoThreadModule>
```

## <a name="remarks"></a>Remarks

`CAtlAutoThreadModule` является производным от [катлаутосреадмодулет](../../atl/reference/catlautothreadmodulet-class.md) и реализует COM-сервер модели подразделения в пуле потоков. `CAtlAutoThreadModule` использует [ккомапартмент](../../atl/reference/ccomapartment-class.md) для управления апартаментом для каждого потока в модуле.

Для указания [ккомклассфакторяутосреад](../../atl/reference/ccomclassfactoryautothread-class.md) в качестве фабрики класса необходимо использовать макрос [DECLARE_CLASSFACTORY_AUTO_THREAD](aggregation-and-class-factory-macros.md#declare_classfactory_auto_thread) в определении класса объекта. Затем следует добавить один экземпляр класса, производного от, `CAtlAutoThreadModuleT` например `CAtlAutoThreadModule` . Пример:

`CAtlAutoThreadModule _AtlAutoModule; // name is immaterial.`

> [!NOTE]
> Этот класс заменяет устаревший класс [ккомаутосреадмодуле](../../atl/reference/ccomautothreadmodule-class.md) .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IAtlAutoThreadModule`

[катлаутосреадмодулет](../../atl/reference/catlautothreadmodulet-class.md)

`CAtlAutoThreadModule`

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="see-also"></a>См. также раздел

[Класс Катлаутосреадмодулет](../../atl/reference/catlautothreadmodulet-class.md)<br/>
[Класс Иатлаутосреадмодуле](../../atl/reference/iatlautothreadmodule-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Классы модулей](../../atl/atl-module-classes.md)
