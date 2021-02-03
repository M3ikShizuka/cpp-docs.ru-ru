---
description: 'Дополнительные сведения о: _bstr_t:: Attach'
title: _bstr_t::Attach
ms.date: 02/02/2021
f1_keywords:
- _bstr_t::Attach
helpviewer_keywords:
- Attach method [C++]
ms.openlocfilehash: 02717fad98e4d68dde70995abcfad4cb55b8c45c
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522889"
---
# `_bstr_t::Attach`

**Блок, относящийся только к системам Microsoft**

Связывает упаковщик `_bstr_t` со строкой `BSTR`.

## <a name="syntax"></a>Синтаксис

```cpp
void Attach(
   BSTR s
);
```

### <a name="parameters"></a>Параметры

*`s`*\
Ресурс `BSTR` для связывания с переменной `_bstr_t` или назначения ей.

## <a name="remarks"></a>Примечания

Если переменная `_bstr_t` была ранее присоединена к другому ресурсу `BSTR`, `_bstr_t` очистит ресурсы `BSTR`, если другие переменные `_bstr_t` не используют `BSTR`.

## <a name="example"></a>Пример

[`_bstr_t::Assign`](../cpp/bstr-t-assign.md)Пример использования см. в разделе **`Attach`** .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`_bstr_t` См](../cpp/bstr-t-class.md)
