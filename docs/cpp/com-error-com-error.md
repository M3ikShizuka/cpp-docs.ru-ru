---
description: 'Дополнительные сведения: _com_error:: _com_error'
title: _com_error::_com_error
ms.date: 11/04/2016
f1_keywords:
- _com_error::_com_error
helpviewer_keywords:
- _com_error method [C++]
ms.assetid: 0a69e46c-caab-49ef-b091-eee401253ce6
ms.openlocfilehash: 2c5b912f5d532e9aed5b8e84a3fe7e2fcd7d4100
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332562"
---
# <a name="_com_error_com_error"></a>_com_error::_com_error

**Блок, относящийся только к системам Microsoft**

Конструирует объект **_com_error** .

## <a name="syntax"></a>Синтаксис

```
_com_error(
   HRESULT hr,
   IErrorInfo* perrinfo = NULL,
   bool fAddRef=false) throw( );

_com_error( const _com_error& that ) throw( );
```

#### <a name="parameters"></a>Параметры

*ч*<br/>
Сведения HRESULT.

*перринфо*<br/>
Объект `IErrorInfo`.

*фаддреф*<br/>
По умолчанию конструктор вызывает AddRef для интерфейса, отличного от NULL `IErrorInfo` . Это обеспечивает правильный подсчет ссылок в общем случае, когда владение интерфейсом передается в объект **_com_error** , например:

```cpp
throw _com_error(hr, perrinfo);
```

Если вы не хотите, чтобы код переносит владение объекту **_com_error** , а `AddRef` требуется смещение в `Release` деструкторе **_com_error** , создайте объект следующим образом:

```cpp
_com_error err(hr, perrinfo, true);
```

*что*<br/>
Существующий объект **_com_error** .

## <a name="remarks"></a>Комментарии

Первый конструктор создает новый объект с заданным значением HRESULT и необязательным `IErrorInfo` объектом. Вторая создает копию существующего объекта **_com_error** .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_error](../cpp/com-error-class.md)
