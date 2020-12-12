---
description: 'Дополнительные сведения о: структура RuntimeClassFlags'
title: RuntimeClassFlags - структура
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::RuntimeClassFlags
- implements/Microsoft::WRL::RuntimeClassFlags::value
helpviewer_keywords:
- Microsoft::WRL::RuntimeClassFlags structure
- Microsoft::WRL::RuntimeClassFlags::value constant
ms.assetid: 7098d605-bd14-4d51-82f4-3def8296a938
ms.openlocfilehash: 7874447fbbbe429884c5a79d0c70bb93e617ec61
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209273"
---
# <a name="runtimeclassflags-structure"></a>RuntimeClassFlags - структура

Содержит тип для экземпляра [RuntimeClass](runtimeclass-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
template <unsigned int flags>
struct RuntimeClassFlags;
```

### <a name="parameters"></a>Параметры

*flags*<br/>
Значение [перечисления RuntimeClassType](runtimeclasstype-enumeration.md) .

## <a name="members"></a>Элементы

### <a name="public-constants"></a>Открытые константы

|Имя|Описание|
|----------|-----------------|
|[Константа RuntimeClassFlags::value](#value-constant)|Содержит значение [перечисления RuntimeClassType](runtimeclasstype-enumeration.md) .|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`RuntimeClassFlags`

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft::WRL

## <a name="runtimeclassflagsvalue-constant"></a><a name="value-constant"></a> Константа RuntimeClassFlags:: value

Поле, содержащее значение [перечисления RuntimeClassType](runtimeclasstype-enumeration.md) .

```cpp
static const unsigned int value = flags;
```
