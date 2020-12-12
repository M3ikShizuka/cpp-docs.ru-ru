---
description: 'Дополнительные сведения о: _variant_t:: ChangeType'
title: _variant_t::ChangeType
ms.date: 11/04/2016
f1_keywords:
- _variant_t::ChangeType
- _variant_t.ChangeType
helpviewer_keywords:
- ChangeType method [C++]
- VARIANT object [C++], ChangeType
- VARIANT object
ms.assetid: 829d2eeb-3338-4a88-9dce-0ca145f47aac
ms.openlocfilehash: 32ce43f1d9afb388c97e5271927113c71d31bb92
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97116630"
---
# <a name="_variant_tchangetype"></a>_variant_t::ChangeType

**Блок, относящийся только к системам Microsoft**

Изменяет тип `_variant_t` объекта на указанный `VARTYPE` .

## <a name="syntax"></a>Синтаксис

```cpp
void ChangeType(
   VARTYPE vartype,
   const _variant_t* pSrc = NULL
);
```

#### <a name="parameters"></a>Параметры

*VarType*<br/>
`VARTYPE`Для этого `_variant_t` объекта.

*pSrc*<br/>
Указатель на объект `_variant_t`, который необходимо преобразовать. Если это значение равно NULL, преобразование выполняется на месте.

## <a name="remarks"></a>Комментарии

Эта функция-член преобразует `_variant_t` объект в указанный `VARTYPE` . Если *pSrc* имеет значение null, преобразование выполняется на месте, в противном случае `_variant_t` объект копируется из *pSrc* и затем преобразуется.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _variant_t](../cpp/variant-t-class.md)
