---
description: Дополнительные сведения о функции GetModuleBase
title: Функция GetModuleBase
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::GetModuleBase
ms.assetid: 123d3b14-2eaf-4e02-8dcd-b6567917c6a6
ms.openlocfilehash: cdedaf905da194400209840b6bd84fa8e626eb0a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295202"
---
# <a name="getmodulebase-function"></a>Функция GetModuleBase

Извлекает указатель [ModuleBase](modulebase-class.md) , позволяющий увеличивать и уменьшать число ссылок объекта [RuntimeClass](runtimeclass-class.md) .

## <a name="syntax"></a>Синтаксис

```cpp
inline Details::ModuleBase* GetModuleBase() throw()
```

## <a name="return-value"></a>Возвращаемое значение

Указатель на объект `ModuleBase`.

## <a name="remarks"></a>Комментарии

Эта внутренняя функция используется для увеличения и уменьшения числа ссылок объекта.

Эту функцию можно использовать для управления счетчиком ссылок путем вызова [ModuleBase:: IncrementObjectCount](modulebase-class.md#incrementobjectcount) и [ModuleBase::D екрементобжекткаунт](modulebase-class.md#decrementobjectcount).

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL](microsoft-wrl-namespace.md)
