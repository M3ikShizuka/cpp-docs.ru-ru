---
description: 'Дополнительные сведения: _com_error:: Source'
title: _com_error::Source
ms.date: 11/04/2016
f1_keywords:
- _com_error::Source
helpviewer_keywords:
- Source method [C++]
ms.assetid: 55353741-fabc-4b0c-9787-b5a69bb189f2
ms.openlocfilehash: 3b6cf35420454e8285d3d8b4deee3df8fe8771e4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295774"
---
# <a name="_com_errorsource"></a>_com_error::Source

**Блок, относящийся только к системам Microsoft**

Вызывает функцию `IErrorInfo::GetSource`.

## <a name="syntax"></a>Синтаксис

```
_bstr_t Source() const;
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает результат `IErrorInfo::GetSource` для `IErrorInfo` объекта, записанного в `_com_error` объекте. Результирующая функция `BSTR` инкапсулируется в объект `_bstr_t`. Если `IErrorInfo` запись не записана, возвращается пустое значение `_bstr_t` .

## <a name="remarks"></a>Комментарии

Любой сбой при вызове `IErrorInfo::GetSource` метода игнорируется.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_error](../cpp/com-error-class.md)
