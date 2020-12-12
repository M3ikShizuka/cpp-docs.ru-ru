---
description: 'Дополнительные сведения: _com_error:: Error'
title: _com_error::Error
ms.date: 11/04/2016
f1_keywords:
- _com_error::Error
- Error
helpviewer_keywords:
- Error method [C++]
ms.assetid: b53a15fd-198e-4276-afcd-13439c4807f7
ms.openlocfilehash: 25dd78caeada9e7606bc26f241126b0d0f510f4c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318199"
---
# <a name="_com_errorerror"></a>_com_error::Error

**Блок, относящийся только к системам Microsoft**

Извлекает значение HRESULT, передаваемое конструктору.

## <a name="syntax"></a>Синтаксис

```
HRESULT Error( ) const throw( );
```

## <a name="return-value"></a>Возвращаемое значение

Необработанный элемент HRESULT, переданный в конструктор.

## <a name="remarks"></a>Комментарии

Извлекает инкапсулированный элемент HRESULT в `_com_error` объекте.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_error](../cpp/com-error-class.md)
