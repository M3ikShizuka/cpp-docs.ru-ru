---
description: Дополнительные сведения о &lt; &gt; функциях List.
title: '&lt;Перечисление &gt; функций | Документация Майкрософт'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- list/std::swap
ms.openlocfilehash: 6a94fcc916db08a510a968b66b0a0dc0cfa9b8e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97284711"
---
# <a name="ltlistgt-functions"></a>&lt;Вывод списка &gt; функций

## <a name="swap"></a><a name="swap"></a> позиции

Меняет местами элементы двух списков.

```cpp
template <class T, class Allocator>
    void swap(list<T, Allocator>& left, list<T, Allocator>& right)
```

### <a name="parameters"></a>Параметры

*слева*\
Объект типа `list`.

*Правильно*\
Объект типа `list`.

### <a name="remarks"></a>Комментарии

Шаблонная функция выполняет `left.swap(right)`.
