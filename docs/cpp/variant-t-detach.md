---
description: 'Дополнительные сведения: _variant_t::D етач'
title: _variant_t::Detach
ms.date: 11/04/2016
f1_keywords:
- _variant_t::Detach
- _variant_t.Detach
helpviewer_keywords:
- VARIANT object [C++], detatch
- Detach method [C++]
- VARIANT object
ms.assetid: c348ac08-62cf-4657-a16f-974a79c12158
ms.openlocfilehash: 502903f73f9b149a5f85a6eb1be44687aab20664
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97204697"
---
# <a name="_variant_tdetach"></a>_variant_t::Detach

**Блок, относящийся только к системам Microsoft**

Отсоединяет инкапсулированный `VARIANT` объект от этого `_variant_t` объекта.

## <a name="syntax"></a>Синтаксис

```
VARIANT Detach( );
```

## <a name="return-value"></a>Возвращаемое значение

Инкапсулированный `VARIANT` .

## <a name="remarks"></a>Комментарии

Извлекает и возвращает инкапсулированный `VARIANT` , а затем очищает этот `_variant_t` объект без его уничтожения. Эта функция члена удаляет `VARIANT` из инкапсуляции и задает `VARTYPE` для этого объекта значение `_variant_t` VT_EMPTY. Для освобождения возвращаемого `VARIANT` метода необходимо вызвать функцию [вариантклеар](/windows/win32/api/oleauto/nf-oleauto-variantclear) .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _variant_t](../cpp/variant-t-class.md)
