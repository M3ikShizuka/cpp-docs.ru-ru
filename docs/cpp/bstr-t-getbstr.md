---
description: 'Дополнительные сведения: _bstr_t:: BSTR'
title: _bstr_t::GetBSTR
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::GetBSTR
helpviewer_keywords:
- GetBSTR method [C++]
ms.openlocfilehash: b48dd082b21c0f3416c8b58b8ae2669c74d9d227
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522759"
---
# `_bstr_t::GetBSTR`

**Блок, относящийся только к системам Microsoft**

Указывает на начало строки `BSTR`, инкапсулированной объектом `_bstr_t`.

## <a name="syntax"></a>Синтаксис

```cpp
BSTR& GetBSTR( );
```

## <a name="return-value"></a>Возвращаемое значение

Начало строки `BSTR`, инкапсулированной объектом `_bstr_t`.

## <a name="remarks"></a>Примечания

**`GetBSTR`** затрагивает все `_bstr_t` объекты, которые совместно используют `BSTR` . `_bstr_t`С помощью `BSTR` конструктора копирования и может совместно использовать несколько экземпляров `operator=` .

## <a name="example"></a>Пример

См [`_bstr_t::Assign`](../cpp/bstr-t-assign.md) . пример, в котором используется **`GetBSTR`** .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` см](../cpp/bstr-t-class.md)