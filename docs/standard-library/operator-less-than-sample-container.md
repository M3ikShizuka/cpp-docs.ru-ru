---
description: 'Дополнительные сведения об операторе: operator &lt; ( &lt; образец контейнера &gt; )'
title: оператор&lt; (&lt;образец контейнера&gt;)
ms.date: 11/04/2016
f1_keywords:
- std::operator<
- operator<
- std.<
- <
- std.operator<
- std::<
helpviewer_keywords:
- < operator, comparing specific objects
- operator<, valarrays
- < operator
- operator <, valarrays
ms.assetid: 31027dd6-53be-428b-b950-1dcb25393597
ms.openlocfilehash: e7bba9be33a2dc4dea6257b159966c867bb33929
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97176487"
---
# <a name="operatorlt-ltsample-containergt"></a>оператор&lt; (&lt;образец контейнера&gt;)

> [!NOTE]
> Эта статья содержится в документации по Microsoft C++ как нефункциональный пример контейнеров, используемых в стандартной библиотеке C++. Дополнительные сведения см. в разделе [Контейнеры стандартной библиотеки C++](../standard-library/stl-containers.md).

Перегрузка **оператора<** для сравнения двух объектов [контейнера](../standard-library/sample-container-class.md)шаблона класса.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
bool operator<(
    const Container <Ty>& left,
    const Container <Ty>& right);
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает `lexicographical_compare(left.begin, left.end, right.begin, right.end)`.

## <a name="see-also"></a>См. также раздел

[\<sample container>](../standard-library/sample-container.md)\
[начале](../standard-library/container-class-begin.md)\
[end](../standard-library/container-class-end.md)
