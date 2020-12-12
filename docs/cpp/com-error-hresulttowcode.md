---
description: 'Дополнительные сведения: _com_error:: Хресулттовкоде'
title: _com_error::HRESULTToWCode
ms.date: 11/04/2016
f1_keywords:
- _com_error::HRESULTToWCode
helpviewer_keywords:
- HRESULTToWCode method [C++]
ms.assetid: ff3789f5-1047-41a0-b7e3-86dd8f638dba
ms.openlocfilehash: 1bbf62be42d4e34a2ef73493f0449c2ffbaf0646
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295838"
---
# <a name="_com_errorhresulttowcode"></a>_com_error::HRESULTToWCode

**Блок, относящийся только к системам Microsoft**

Сопоставляет 32-разрядное значение HRESULT с 16-разрядным `wCode` .

## <a name="syntax"></a>Синтаксис

```
static WORD HRESULTToWCode(
   HRESULT hr
) throw( );
```

#### <a name="parameters"></a>Параметры

*ч*<br/>
32-разрядное значение HRESULT, которое должно быть сопоставлено с 16-битным значением `wCode` .

## <a name="return-value"></a>Возвращаемое значение

16-разрядный `wCode` параметр, сопоставленный с 32-битным значением HRESULT.

## <a name="remarks"></a>Комментарии

Дополнительные сведения см. в разделе [_com_error:: wCode](../cpp/com-error-wcode.md) .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[_com_error::WCode](../cpp/com-error-wcode.md)<br/>
[_com_error::WCodeToHRESULT](../cpp/com-error-wcodetohresult.md)<br/>
[Класс _com_error](../cpp/com-error-class.md)
