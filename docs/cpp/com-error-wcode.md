---
description: 'Дополнительные сведения: _com_error:: WCode'
title: _com_error::WCode
ms.date: 11/04/2016
f1_keywords:
- _com_error::WCode
helpviewer_keywords:
- WCode method [C++]
ms.assetid: f3b21852-f8ea-4e43-bff1-11c2d35454c4
ms.openlocfilehash: e3a19e5ae6c98cb38445e5eaa822474b2a852135
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295735"
---
# <a name="_com_errorwcode"></a>_com_error::WCode

**Блок, относящийся только к системам Microsoft**

Извлекает 16-разрядный код ошибки, сопоставленный с инкапсулированным значением HRESULT.

## <a name="syntax"></a>Синтаксис

```
WORD WCode ( ) const throw( );
```

## <a name="return-value"></a>Возвращаемое значение

Если значение HRESULT находится в диапазоне от 0x80040200 до 0x8004FFFF, `WCode` метод возвращает значение HRESULT минус 0x80040200. в противном случае возвращается ноль.

## <a name="remarks"></a>Комментарии

`WCode`Метод используется для отмены сопоставления, происходящего в коде поддержки COM. Оболочка для `dispinterface` свойства или метода вызывает подпрограмму поддержки, которая упаковывает аргументы и вызывает `IDispatch::Invoke` . При возврате, если возвращается ошибка HRESULT of `DISP_E_EXCEPTION` , сведения об ошибке извлекаются из `EXCEPINFO` структуры, передаваемой в `IDispatch::Invoke` . Код ошибки может быть 16-битным значением, хранящимся в элементе `wCode` `EXCEPINFO` структуры, или полным 32-битным значением в элементе `scode` `EXCEPINFO` структуры. Если возвращается 16-разрядный объект `wCode` , он сначала должен быть сопоставлен с ЗНАЧЕНИЕМ HRESULT 32-разрядного сбоя.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[_com_error::HRESULTToWCode](../cpp/com-error-hresulttowcode.md)<br/>
[_com_error::WCodeToHRESULT](../cpp/com-error-wcodetohresult.md)<br/>
[Класс _com_error](../cpp/com-error-class.md)
