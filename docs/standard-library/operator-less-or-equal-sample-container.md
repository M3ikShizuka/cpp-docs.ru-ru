---
description: 'Дополнительные сведения: operator &lt; = ( &lt; образец контейнера &gt; )'
title: оператор&lt;= (&lt;образец контейнера&gt;)
ms.date: 11/04/2016
f1_keywords:
- std::<=
- std.operator<=
- operator<=
- std.<=
- std::operator<=
- <=
helpviewer_keywords:
- operator<=
- operator <=
- <= operator, with specific objects
- <= operator
ms.assetid: 338577dd-dc88-4a2b-9e12-0379c54fc8a2
ms.openlocfilehash: 4455efcbd5b3ccca262265f44414b46d3e97f57d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337996"
---
# <a name="operatorlt-ltsample-containergt"></a>оператор&lt;= (&lt;образец контейнера&gt;)

> [!NOTE]
> Эта статья содержится в документации по Microsoft C++ как нефункциональный пример контейнеров, используемых в стандартной библиотеке C++. Дополнительные сведения см. в разделе [Контейнеры стандартной библиотеки C++](../standard-library/stl-containers.md).

Перегрузка **оператора<=** для сравнения двух объектов [контейнера](../standard-library/sample-container-class.md)шаблона класса.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
bool operator<=(
    const Container <Ty>& left,
    const Container <Ty>& right);
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает `!(right < left)`.

## <a name="see-also"></a>См. также раздел

[\<sample container>](../standard-library/sample-container.md)
