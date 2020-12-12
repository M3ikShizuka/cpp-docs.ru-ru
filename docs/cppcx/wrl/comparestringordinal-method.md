---
description: Дополнительные сведения о методе CompareStringOrdinal
title: Метод CompareStringOrdinal
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Details::CompareStringOrdinal
ms.assetid: ffa997fd-8cd7-40a5-b9e7-f55d40b072f4
ms.openlocfilehash: 1994d0f3ec4104e27094de10255194a911ae2945
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97282852"
---
# <a name="comparestringordinal-method"></a>Метод CompareStringOrdinal

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
inline INT32 CompareStringOrdinal(
   HSTRING lhs,
   HSTRING rhs)
```

### <a name="parameters"></a>Параметры

*LHS*<br/>
Первый HSTRING для сравнения.

*rhs*<br/>
Второй HSTRING для сравнения.

## <a name="return-value"></a>Возвращаемое значение

|Значение|Условие|
|-----------|---------------|
|-1|*LHS* меньше, чем *RHS*.|
|0|*LHS* равняется *RHS*.|
|1|*LHS* больше, чем *RHS*.|

## <a name="remarks"></a>Комментарии

Сравнивает два указанных объекта HSTRING и возвращает целое число, которое указывает их относительное расположение в порядке сортировки.

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Microsoft:: WRL:: оболочки::D состояния

## <a name="see-also"></a>См. также раздел

[Microsoft:: WRL:: оболочки::D пространство имен состояния](microsoft-wrl-wrappers-details-namespace.md)
