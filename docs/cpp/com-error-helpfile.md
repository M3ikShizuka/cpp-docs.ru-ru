---
description: 'Дополнительные сведения: _com_error:: HelpFile'
title: _com_error::HelpFile
ms.date: 11/04/2016
f1_keywords:
- _com_error::HelpFile
helpviewer_keywords:
- HelpFile method [C++]
ms.assetid: d2d3a0a1-6b62-4d52-a818-3cfae545a4af
ms.openlocfilehash: e45785913a8a5a1909f702bce672727171e0baef
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295930"
---
# <a name="_com_errorhelpfile"></a>_com_error::HelpFile

**Блок, относящийся только к системам Microsoft**

Вызывает функцию `IErrorInfo::GetHelpFile`.

## <a name="syntax"></a>Синтаксис

```
_bstr_t HelpFile() const;
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает результат `IErrorInfo::GetHelpFile` для `IErrorInfo` объекта, записанного в `_com_error` объекте. Результирующая строка BSTR инкапсулируется в объект `_bstr_t`. Если `IErrorInfo` запись не записана, возвращается пустое значение `_bstr_t` .

## <a name="remarks"></a>Комментарии

Любой сбой при вызове `IErrorInfo::GetHelpFile` метода игнорируется.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_error](../cpp/com-error-class.md)
