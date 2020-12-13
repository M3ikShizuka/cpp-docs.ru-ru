---
description: 'Дополнительные сведения: _com_error::D Описание'
title: _com_error::Description
ms.date: 11/04/2016
f1_keywords:
- _com_error::Description
helpviewer_keywords:
- Description method [C++]
ms.assetid: 88191e24-4ee8-44a6-8c4c-3758e22e0548
ms.openlocfilehash: 6404d16361abe81d9e234a6b63039a7476d91ef1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332558"
---
# <a name="_com_errordescription"></a>_com_error::Description

**Блок, относящийся только к системам Microsoft**

Вызывает функцию `IErrorInfo::GetDescription`.

## <a name="syntax"></a>Синтаксис

```
_bstr_t Description( ) const;
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает результат `IErrorInfo::GetDescription` для `IErrorInfo` объекта, записанного в `_com_error` объекте. Результирующая функция `BSTR` инкапсулируется в объект `_bstr_t`. Если `IErrorInfo` запись не записана, возвращается пустое значение `_bstr_t` .

## <a name="remarks"></a>Комментарии

Вызывает `IErrorInfo::GetDescription` функцию и получает `IErrorInfo` запись в `_com_error` объект. Любой сбой при вызове `IErrorInfo::GetDescription` метода игнорируется.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_error](../cpp/com-error-class.md)
