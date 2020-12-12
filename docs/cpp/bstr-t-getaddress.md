---
description: 'Дополнительные сведения о: _bstr_t::/Address'
title: _bstr_t::GetAddress
ms.date: 11/04/2016
f1_keywords:
- _bstr_t::GetAddress
helpviewer_keywords:
- GetAddress method [C++]
ms.assetid: 09bc9180-867e-4ee5-b22a-8339dc663142
ms.openlocfilehash: afb877a6f1b4cfcfb6fe08b36168af745d733b85
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97229318"
---
# <a name="_bstr_tgetaddress"></a>_bstr_t::GetAddress

**Блок, относящийся только к системам Microsoft**

Освобождает любую существующую строку и возвращает адрес новой строки, которой была выделена память.

## <a name="syntax"></a>Синтаксис

```
BSTR* GetAddress( );
```

## <a name="return-value"></a>Возвращаемое значение

Указатель на строку `BSTR`, инкапсулированную объектом `_bstr_t`.

## <a name="remarks"></a>Комментарии

Действие " **Субадрес** " влияет на все `_bstr_t` объекты, совместно использующие `BSTR` . `_bstr_t`С помощью `BSTR` конструктора копирования и **оператора =** могут совместно использовать несколько экземпляров.

## <a name="example"></a>Пример

Пример использования метода- **Address** см. в разделе [_Bstr_t:: Assign](../cpp/bstr-t-assign.md) .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _bstr_t](../cpp/bstr-t-class.md)
