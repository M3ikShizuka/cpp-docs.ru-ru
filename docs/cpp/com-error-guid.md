---
description: 'Дополнительные сведения: _com_error:: GUID'
title: _com_error::GUID
ms.date: 11/04/2016
f1_keywords:
- _com_error::GUID
helpviewer_keywords:
- GUID method [C++]
ms.assetid: e84c2c23-d02e-48f8-b776-9bd6937296d2
ms.openlocfilehash: 32f88728d5c0f93094413aaeae8fb3c116b415c3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295969"
---
# <a name="_com_errorguid"></a>_com_error::GUID

**Блок, относящийся только к системам Microsoft**

Вызывает функцию `IErrorInfo::GetGUID`.

## <a name="syntax"></a>Синтаксис

```
GUID GUID( ) const throw( );
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает результат `IErrorInfo::GetGUID` для `IErrorInfo` объекта, записанного в `_com_error` объекте. Если `IErrorInfo` объект не записан, возвращается значение `GUID_NULL` .

## <a name="remarks"></a>Комментарии

Любой сбой при вызове `IErrorInfo::GetGUID` метода игнорируется.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_error](../cpp/com-error-class.md)
