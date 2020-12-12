---
description: 'Дополнительные сведения о: хэш-структура (стандартная библиотека C++)'
title: Структура hash (Стандартная библиотека C++) | Документы Майкрософт
ms.date: 11/04/2016
f1_keywords:
- thread/std::hash
ms.assetid: 4a8bf5bc-4334-4070-936b-98585f8a073b
ms.openlocfilehash: 095566b6855c837c3ee6049a5cbedfbb087420bb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324072"
---
# <a name="hash-structure-c-standard-library"></a>Структура hash (Стандартная библиотека C++)

Определяет функцию-член, возвращающую значение, которое уникально определяется с помощью `Val`. Функция-член определяет функцию [hash](../standard-library/hash-class.md), которую можно использовать для сопоставления значений типа `thread::id` с распределением значений индекса.

## <a name="syntax"></a>Синтаксис

```cpp
template <>
struct hash<thread::id> :
    public unary_function<thread::id, size_t>
{
    size_t operator()(thread::id Val) const;

};
```

## <a name="requirements"></a>Требования

**Заголовок:**\<thread>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[\<thread>](../standard-library/thread.md)\
[Структура unary_function](../standard-library/unary-function-struct.md)
