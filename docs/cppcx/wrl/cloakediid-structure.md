---
description: 'Дополнительные сведения о: структура Клоакедиид'
title: CloakedIid - структура
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::CloakedIid
helpviewer_keywords:
- CloakedIid structure
ms.assetid: 82e0e377-ca3a-46bc-b850-ae2c46c15bb5
ms.openlocfilehash: 06bddded27882ae1216064aafc311364a8d2fd9f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338782"
---
# <a name="cloakediid-structure"></a>CloakedIid - структура

Указывает на `RuntimeClass` , а также на `Implements` шаблоны, `ChainInterfaces` которые указанный интерфейс недоступен в списке IID.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename T>
struct CloakedIid : T;
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Скрытый (замаскированный) интерфейс.

## <a name="remarks"></a>Комментарии

Ниже приведен пример использования **клоакедиид** : `struct MyRuntimeClass : RuntimeClass<CloakedIid<IMyCloakedInterface>> {}` .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`T`

`CloakedIid`

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL](microsoft-wrl-namespace.md)
