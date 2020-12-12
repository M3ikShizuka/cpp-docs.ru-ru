---
description: 'Дополнительные сведения: класс контейнера:: Erase'
title: Класс контейнера::erase
ms.date: 11/04/2016
helpviewer_keywords:
- erase method
ms.assetid: abc091c5-5a80-4bd8-93a8-a2d9bde2efec
ms.openlocfilehash: 7e9d7747237a38c42bfb7a39c5d5e66cc8a44608
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324871"
---
# <a name="container-classerase"></a>Класс контейнера::erase

> [!NOTE]
> Эта статья содержится в документации по Microsoft C++ как нефункциональный пример контейнеров, используемых в стандартной библиотеке C++. Дополнительные сведения см. в разделе [Контейнеры стандартной библиотеки C++](../standard-library/stl-containers.md).

Удаляет элемент.

## <a name="syntax"></a>Синтаксис

```cpp
iterator erase(
    iterator _Where);

iterator erase(
    iterator first,
    iterator last);
```

## <a name="remarks"></a>Remarks

Первая функция члена удаляет элемент управляемой последовательности, на которую указывает *_Where*. Вторая функция-член удаляет элементы управляемой последовательности в диапазоне [`first`, `last`). Обе возвращают итератор, который обозначает первый элемент, находящийся за всеми удаленными элементами, или [end](../standard-library/container-class-end.md), если такой элемент не существует.

Функции-члены вызывают исключение только в том случае, если операция копирования создает исключение.

## <a name="see-also"></a>См. также раздел

[Пример класса контейнера](../standard-library/sample-container-class.md)
