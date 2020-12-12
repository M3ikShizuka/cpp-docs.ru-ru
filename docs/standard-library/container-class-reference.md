---
description: 'Дополнительные сведения: класс контейнера:: Reference'
title: Класс контейнера::reference
ms.date: 11/04/2016
helpviewer_keywords:
- reference method
ms.assetid: ab85a9fb-c628-4761-9a5f-a0231fad7690
ms.openlocfilehash: e3a143ec9a195f7ea42f3b067a72b40ef5be9283
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324845"
---
# <a name="container-classreference"></a>Класс контейнера::reference

> [!NOTE]
> Эта статья содержится в документации по Microsoft C++ как нефункциональный пример контейнеров, используемых в стандартной библиотеке C++. Дополнительные сведения см. в разделе [Контейнеры стандартной библиотеки C++](../standard-library/stl-containers.md).

Описывает объект, который можно использовать в качестве ссылки на элемент управляемой последовательности.

## <a name="syntax"></a>Синтаксис

```cpp
typedef T2 reference;
```

## <a name="remarks"></a>Remarks

Он описан здесь как синоним для неопределенного типа `T2` (обычно `Alloc::reference` ). Объект типа `reference` можно привести к объекту типа [const_reference](../standard-library/container-class-const-reference.md).

## <a name="see-also"></a>См. также раздел

[Пример класса контейнера](../standard-library/sample-container-class.md)
