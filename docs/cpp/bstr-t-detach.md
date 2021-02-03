---
description: 'Дополнительные сведения: _bstr_t::D етач'
title: _bstr_t::Detach
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::Detach
helpviewer_keywords:
- Detach method [C++]
ms.openlocfilehash: bc269f46d3a393485e95a62df23692c60070d75a
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522850"
---
# `_bstr_t::Detach`

**Блок, относящийся только к системам Microsoft**

Возвращает строку `BSTR`, инкапсулированную объектом `_bstr_t`, и отсоединяет ее (`BSTR`) от этого объекта (`_bstr_t`).

## <a name="syntax"></a>Синтаксис

```cpp
BSTR Detach( ) throw;
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект, `BSTR` инкапсулированный в `_bstr_t` .

## <a name="example"></a>Пример

См [`_bstr_t::Assign`](../cpp/bstr-t-assign.md) . пример, в котором используется **`Detach`** .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)
