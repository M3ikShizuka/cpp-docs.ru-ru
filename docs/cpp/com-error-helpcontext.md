---
description: 'Дополнительные сведения о: _com_error:: HelpContext'
title: _com_error::HelpContext
ms.date: 11/04/2016
f1_keywords:
- _com_error::HelpContext
helpviewer_keywords:
- HelpContext method [C++]
ms.assetid: 160d6443-9b68-4cf5-a540-50da951a5b2b
ms.openlocfilehash: 757fb572d9e41486af419712eb7f70cd7cfa7b14
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295943"
---
# <a name="_com_errorhelpcontext"></a>_com_error::HelpContext

**Блок, относящийся только к системам Microsoft**

Вызывает функцию `IErrorInfo::GetHelpContext`.

## <a name="syntax"></a>Синтаксис

```
DWORD HelpContext( ) const throw( );
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает результат `IErrorInfo::GetHelpContext` для `IErrorInfo` объекта, записанного в `_com_error` объекте. Если `IErrorInfo` объект не записан, возвращается ноль.

## <a name="remarks"></a>Комментарии

Любой сбой при вызове `IErrorInfo::GetHelpContext` метода игнорируется.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_error](../cpp/com-error-class.md)
