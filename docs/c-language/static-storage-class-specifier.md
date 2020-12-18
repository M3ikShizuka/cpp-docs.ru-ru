---
description: Подробнее об описателе класса хранения static
title: Спецификатор класса хранения static
ms.date: 11/04/2016
helpviewer_keywords:
- static variables, specifier
- storage classes, static
- static storage class specifiers
ms.assetid: 9bce361e-919b-46b9-8148-40d7ab0eb024
ms.openlocfilehash: da7ca4ea71b3e450da986ec175adcaf08852d81b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97168752"
---
# <a name="static-storage-class-specifier"></a>Спецификатор класса хранения static

Переменная, объявленная на внутреннем уровне с помощью описателя класса хранения **`static`** , имеет глобальное время существования, но доступна только внутри блока, в котором она объявлена. Описатель **`static`** полезно использовать в константных строках, потому что при этом снимается нагрузка частой инициализации в часто вызываемых функциях.

## <a name="remarks"></a>Примечания

Если переменная с типом **`static`** не инициализирована явно, она инициализируется со значением 0 по умолчанию. Внутри функции **`static`** выделяет хранилище и служит определением. Внутренние статические переменные представляют закрытое постоянное хранилище, видимое только одной функции.

## <a name="see-also"></a>См. также

[Классы хранения в C](c-storage-classes.md)<br/>
[Storage classes (C++)](../cpp/storage-classes-cpp.md) (Классы хранения (C++))
