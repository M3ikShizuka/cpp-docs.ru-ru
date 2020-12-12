---
description: 'Дополнительные сведения: класс контейнера:: swap'
title: Класс контейнера::swap
ms.date: 11/04/2016
helpviewer_keywords:
- swap method
ms.assetid: 898c219c-bc8e-4d14-a149-6240426c693f
ms.openlocfilehash: a38dd6d14ada3ad50927060ccec1542ebf2fd4ca
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97233361"
---
# <a name="container-classswap"></a>Класс контейнера::swap

> [!NOTE]
> Эта статья содержится в документации по Microsoft C++ как нефункциональный пример контейнеров, используемых в стандартной библиотеке C++. Дополнительные сведения см. в разделе [Контейнеры стандартной библиотеки C++](../standard-library/stl-containers.md).

Меняет местами управляемые последовательности между **\* этим** и его аргументом.

## <a name="syntax"></a>Синтаксис

```cpp
void swap(Container& right);
```

## <a name="remarks"></a>Remarks

Если **\* это. Get \_ распределителя = =** _right_**.get_allocator**, он выполняет переключение в постоянное время. В противном случае она выполняет ряд назначений элементов и вызовов конструктора, пропорционально количеству элементов в двух управляемых последовательностях.

## <a name="see-also"></a>См. также раздел

[Пример класса контейнера](../standard-library/sample-container-class.md)
