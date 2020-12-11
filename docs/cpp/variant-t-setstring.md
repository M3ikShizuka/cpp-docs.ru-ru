---
description: 'Дополнительные сведения: _variant_t:: SetString'
title: _variant_t::SetString
ms.date: 11/04/2016
f1_keywords:
- _variant_t::SetString
helpviewer_keywords:
- SetString method [C++]
ms.assetid: 816b08e5-6830-46ca-b3d7-7689308b3be3
ms.openlocfilehash: a36bab9189b6046325bb275469dc9dbdb495fc7a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97161420"
---
# <a name="_variant_tsetstring"></a>_variant_t::SetString

**Блок, относящийся только к системам Microsoft**

Присваивает строку данному объекту `_variant_t`.

## <a name="syntax"></a>Синтаксис

```cpp
void SetString(const char* pSrc);
```

#### <a name="parameters"></a>Параметры

*pSrc*<br/>
Указатель на строку знаков.

## <a name="remarks"></a>Комментарии

Преобразует символьную строку ANSI в строку `BSTR` Юникода и присваивает ее данному объекту `_variant_t`.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _variant_t](../cpp/variant-t-class.md)
