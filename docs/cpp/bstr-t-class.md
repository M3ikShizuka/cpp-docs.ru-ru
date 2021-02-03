---
title: _bstr_t - класс
description: 'Дополнительные сведения о: _bstr_t классе'
ms.date: 02/02/2021
f1_keywords:
- _bstr_t
helpviewer_keywords:
- BSTR object
- _bstr_t class
- BSTR object [C++], COM encapsulation
ms.openlocfilehash: 71f5f0a27989b416cf4f13873254890db09ce334
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522876"
---
# <a name="_bstr_t-class"></a>Класс `_bstr_t`

**Блок, относящийся только к системам Microsoft**

`_bstr_t`Объект инкапсулирует [тип данных BSTR](/previous-versions/windows/desktop/automat/bstr). Класс управляет выделением и освобождением ресурсов с помощью вызовов функций [`SysAllocString`](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) и [`SysFreeString`](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) других `BSTR` API, если это уместно. `_bstr_t`Класс использует подсчет ссылок во избежание чрезмерных издержек.

## <a name="members"></a>Участники

### <a name="construction"></a>Строительство

| Конструктор | Описание |
|--|--|
| [`_bstr_t`](../cpp/bstr-t-bstr-t.md) | Формирует объект `_bstr_t`. |

### <a name="operations"></a>Операции

| Функция | Описание |
|--|--|
| [`Assign`](../cpp/bstr-t-assign.md) | Копирует строку `BSTR` в строку `BSTR`, инкапсулированную объектом `_bstr_t`. |
| [`Attach`](../cpp/bstr-t-attach.md) | Связывает упаковщик `_bstr_t` со строкой `BSTR`. |
| [`copy`](../cpp/bstr-t-copy.md) | Создает копию инкапсулированного объекта `BSTR`. |
| [`Detach`](../cpp/bstr-t-detach.md) | Возвращает строку `BSTR`, инкапсулированную объектом `_bstr_t`, и отсоединяет ее (`BSTR`) от этого объекта (`_bstr_t`). |
| [`GetAddress`](../cpp/bstr-t-getaddress.md) | Указывает на строку `BSTR`, инкапсулированную объектом `_bstr_t`. |
| [`GetBSTR`](../cpp/bstr-t-getbstr.md) | Указывает на начало строки `BSTR`, инкапсулированной объектом `_bstr_t`. |
| [`length`](../cpp/bstr-t-length.md) | Возвращает число символов в объекте `_bstr_t`. |

### <a name="operators"></a>Операторы

| Оператор | Описание |
|--|--|
| [`operator =`](../cpp/bstr-t-operator-equal.md) | Присваивает новое значение существующему объекту `_bstr_t`. |
| [`operator +=`](../cpp/bstr-t-operator-add-equal-plus.md) | Добавляет символы в конец объекта `_bstr_t`. |
| [`operator +`](../cpp/bstr-t-operator-add-equal-plus.md) | Объединяет две строки. |
| [`operator !`](../cpp/bstr-t-operator-logical-not.md) | Проверяет, является ли Инкапсулированная `BSTR` строка пустой. |
| [`operator ==`](../cpp/bstr-t-relational-operators.md)<br/>[`operator !=`](../cpp/bstr-t-relational-operators.md)<br/>[`operator <`](../cpp/bstr-t-relational-operators.md)<br/>[`operator >`](../cpp/bstr-t-relational-operators.md)<br/>[`operator <=`](../cpp/bstr-t-relational-operators.md)<br/>[`operator >=`](../cpp/bstr-t-relational-operators.md) | Сравнивает два объекта `_bstr_t`. |
| [`operator wchar_t*`](../cpp/bstr-t-wchar-t-star-bstr-t-char-star.md)<br/>[`operator char*`](../cpp/bstr-t-wchar-t-star-bstr-t-char-star.md)  | Извлекает указатели на инкапсулированный объект Юникода или многобайтовый объект `BSTR`. |

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="requirements"></a>Требования

**Заголовок:**\<comutil.h>

**Библиотека:** *`comsuppw.lib`* или *`comsuppwd.lib`* (Дополнительные сведения см. в разделе [ `/Zc:wchar_t` (wchar_t является собственным типом)](../build/reference/zc-wchar-t-wchar-t-is-native-type.md)).

## <a name="see-also"></a>См. также

[Классы поддержки COM компилятора](../cpp/compiler-com-support-classes.md)
