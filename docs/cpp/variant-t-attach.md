---
description: 'Дополнительные сведения о: _variant_t:: Attach'
title: _variant_t::Attach
ms.date: 11/04/2016
f1_keywords:
- _variant_t::Attach
- _variant_t.Attach
helpviewer_keywords:
- Attach method [C++]
- VARIANT object [C++], attach
- VARIANT object
ms.assetid: 2f02bd08-2306-4477-aa88-d2a5dee2b859
ms.openlocfilehash: de13b1e8138eb24971e52165ee84fc92d97ca3d9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97116656"
---
# <a name="_variant_tattach"></a>_variant_t::Attach

**Блок, относящийся только к системам Microsoft**

Присоединяет `VARIANT` объект к объекту **_variant_t** .

## <a name="syntax"></a>Синтаксис

```cpp
void Attach(VARIANT& varSrc);
```

#### <a name="parameters"></a>Параметры

*varSrc*<br/>
`VARIANT`Объект, присоединяемый к этому **_variant_t** объекту.

## <a name="remarks"></a>Комментарии

Принимает владение `VARIANT` объектом, инкапсулирующий его. Эта функция члена освобождает все существующие инкапсулированные `VARIANT` , затем копирует предоставленный объект `VARIANT` и присваивает свойству `VARTYPE` значение VT_EMPTY, чтобы убедиться, что его ресурсы можно освободить только с помощью деструктора **_variant_t** .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _variant_t](../cpp/variant-t-class.md)
