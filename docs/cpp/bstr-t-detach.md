---
description: 'Дополнительные сведения: _bstr_t::D етач'
title: _bstr_t::Detach
ms.date: 11/04/2016
f1_keywords:
- _bstr_t::Detach
helpviewer_keywords:
- Detach method [C++]
ms.assetid: cc8284bd-f68b-4fff-b2e6-ce8354dabf8b
ms.openlocfilehash: 0baa246e8a849a9cfb747a4a7e224ecbec328d0a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97229331"
---
# <a name="_bstr_tdetach"></a>_bstr_t::Detach

**Блок, относящийся только к системам Microsoft**

Возвращает строку `BSTR`, инкапсулированную объектом `_bstr_t`, и отсоединяет ее (`BSTR`) от этого объекта (`_bstr_t`).

## <a name="syntax"></a>Синтаксис

```
BSTR Detach( ) throw;
```

## <a name="return-value"></a>Возвращаемое значение

`BSTR` в оболочке `_bstr_t`.

## <a name="example"></a>Пример

См. раздел [_bstr_t:: Assign](../cpp/bstr-t-assign.md) для примера с помощью **отсоединения**.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _bstr_t](../cpp/bstr-t-class.md)
