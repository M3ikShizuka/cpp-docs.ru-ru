---
description: 'Дополнительные сведения: _bstr_t:: BSTR'
title: _bstr_t::GetBSTR
ms.date: 11/04/2016
f1_keywords:
- _bstr_t::GetBSTR
helpviewer_keywords:
- GetBSTR method [C++]
ms.assetid: 0c62ff16-4433-4183-a03c-d5a0a9b731ef
ms.openlocfilehash: ced985bb5123d86ff119279fc49a2b4d181ba8b3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97229305"
---
# <a name="_bstr_tgetbstr"></a>_bstr_t::GetBSTR

**Блок, относящийся только к системам Microsoft**

Указывает на начало строки `BSTR`, инкапсулированной объектом `_bstr_t`.

## <a name="syntax"></a>Синтаксис

```
BSTR& GetBSTR( );
```

## <a name="return-value"></a>Возвращаемое значение

Начало строки `BSTR`, инкапсулированной объектом `_bstr_t`.

## <a name="remarks"></a>Комментарии

В. **BSTR** влияет на все `_bstr_t` объекты, совместно использующие `BSTR` . `_bstr_t`С помощью `BSTR` конструктора копирования и **оператора =** могут совместно использовать несколько экземпляров.

## <a name="example"></a>Пример

См. раздел [_bstr_t:: Assign](../cpp/bstr-t-assign.md) в качестве примера с помощью функции **BSTR**.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _bstr_t](../cpp/bstr-t-class.md)
