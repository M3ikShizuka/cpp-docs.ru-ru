---
description: 'Дополнительные сведения о: _bstr_t::/Address'
title: _bstr_t::GetAddress
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::GetAddress
helpviewer_keywords:
- GetAddress method [C++]
ms.openlocfilehash: 23013a6666b8e268a6437532b69050933ffe6b42
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522837"
---
# `_bstr_t::GetAddress`

**Блок, относящийся только к системам Microsoft**

Освобождает любую существующую строку и возвращает адрес новой строки, которой была выделена память.

## <a name="syntax"></a>Синтаксис

```cpp
BSTR* GetAddress( );
```

## <a name="return-value"></a>Возвращаемое значение

Указатель на строку `BSTR`, инкапсулированную объектом `_bstr_t`.

## <a name="remarks"></a>Примечания

**`GetAddress`** затрагивает все `_bstr_t` объекты, которые совместно используют `BSTR` . `_bstr_t`С помощью `BSTR` конструктора копирования и может совместно использовать несколько экземпляров **`operator=`** .

## <a name="example"></a>Пример

См [`_bstr_t::Assign`](../cpp/bstr-t-assign.md) . пример, в котором используется **`GetAddress`** .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)