---
description: 'Дополнительные сведения: примеры членов контейнера'
title: Члены образца контейнера
ms.date: 11/04/2016
helpviewer_keywords:
- container classes
ms.assetid: dc5a1998-a31b-4adf-b888-8abe5b87a4e0
ms.openlocfilehash: fabf049f3fd33483cd226fd541717c7ac6d6df29
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97269202"
---
# <a name="sample-container-members"></a>Члены образца контейнера

> [!NOTE]
> Эта статья содержится в документации по Microsoft C++ как нефункциональный пример контейнеров, используемых в стандартной библиотеке C++. Дополнительные сведения см. в разделе [Контейнеры стандартной библиотеки C++](../standard-library/stl-containers.md).

## <a name="reference"></a>Ссылка

## <a name="typedefs"></a>Определения типов

|Имя|Описание|
|-|-|
|[const_iterator](../standard-library/container-class-const-iterator.md)|Описывает объект, который можно использовать в качестве постоянного итератора для управляемой последовательности.|
|[const_reference](../standard-library/container-class-const-reference.md)|Описывает объект, который можно использовать в качестве постоянной ссылки на элемент управляемой последовательности.|
|[const_reverse_iterator](../standard-library/container-class-const-reverse-iterator.md)|Описывает объект, который можно использовать в качестве постоянного обратного итератора для управляемой последовательности.|
|[difference_type](../standard-library/container-class-difference-type.md)|Описывает объект, который может представлять разницу между адресами любых двух элементов в управляемой последовательности.|
|[iterator](../standard-library/container-class-iterator.md)|Описывает объект, который можно использовать в качестве итератора для управляемой последовательности.|
|[reference](../standard-library/container-class-reference.md)|Описывает объект, который можно использовать в качестве ссылки на элемент управляемой последовательности.|
|[reverse_iterator](../standard-library/container-class-reverse-iterator.md)|Описывает объект, который можно использовать в качестве обратного итератора для управляемой последовательности.|
|[size_type](../standard-library/container-class-size-type.md)|Описывает объект, который может представлять длину любой управляемой последовательности.|
|[value_type](../standard-library/container-class-value-type.md)|Выполняет синоним для параметра-шаблона `Ty` .|

## <a name="member-functions"></a>Функции элементов

|Имя|Описание|
|-|-|
|[начале](../standard-library/container-class-begin.md)|Возвращает итератор, указывающий на первый элемент последовательности (или на место сразу за концом пустой последовательности).|
|[пусто](../standard-library/container-class-clear.md)|Вызывает метод [erase](../standard-library/container-class-erase.md)( [begin](../standard-library/container-class-begin.md), [end](../standard-library/container-class-end.md)).|
|[empty](../standard-library/container-class-empty.md)|Возвращает **`true`** для пустой управляемой последовательности.|
|[end](../standard-library/container-class-end.md)|Возвращает итератор, который указывает на позицию непосредственно за концом последовательности.|
|[erase](../standard-library/container-class-erase.md)|Удаляет элемент.|
|[max_size](../standard-library/container-class-max-size.md)|Возвращает длину самой длинной последовательности, которая может контролироваться объектом, в постоянном времени независимо от длины управляемой последовательности.|
|[rbegin](../standard-library/container-class-rbegin.md)|Возвращает обратный итератор, который указывает на позицию за концом управляемой последовательности, обозначая начало обратной последовательности.|
|[rend](../standard-library/container-class-rend.md)|Функция-член возвращает обратный итератор, указывающий на первый элемент последовательности (или на место сразу за концом пустой последовательности), обозначая конец обратной последовательности.|
|[size](../standard-library/container-class-size.md)|Возвращает длину управляемой последовательности в постоянном времени независимо от длины управляемой последовательности.|
|[позиции](../standard-library/container-class-swap.md)
