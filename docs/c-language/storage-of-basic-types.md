---
description: 'Подробнее о следующем: Хранилище базовых типов'
title: Хранилище базовых типов
ms.date: 10/02/2019
helpviewer_keywords:
- specifiers [C++], type
- integral types, storage
- storage [C++], types
- floating-point numbers, storage
- type specifiers [C++], sizes
- arithmetic operations [C++], types
- int data type
- short data type
- signed types [C++], storage
- long double keyword [C], storage
- long keyword [C]
- double data type, storage
- types [C], arithmetic
- integral types
- data types [C], specifiers
- storing types [C++]
- unsigned types [C++], storage
- data types [C], storage
ms.assetid: bd1f33c1-c6b9-4558-8a72-afb21aef3318
ms.openlocfilehash: c8ae057de19e04327491fd73e45bcd32c1db7738
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97296645"
---
# <a name="storage-of-basic-types"></a>Хранилище базовых типов

В следующей таблице перечислены хранилища, связанные с каждым базовым типом.

## <a name="sizes-of-fundamental-types"></a>Размеры основных типов

|Type|Хранилище|
|----------|-------------|
|**`char`**, **`unsigned char`**, **`signed char`**|1 байт|
|**`short`**, **`unsigned short`**|2 байта|
|**`int`**, **`unsigned int`**|4 байта|
|**`long`**, **`unsigned long`**|4 байта|
|**`long long`**, **`unsigned long long`**|8 байт|
|**`float`**|4 байта|
|**`double`**|8 байт|
|**`long double`**|8 байт|

Типы данных C разделяются на общие категории. *Целочисленные типы* включают в себя **`int`** , **`char`** , **`short`** , **`long`** и **`long long`** . Такие типы могут иметь уточнение **`signed`** или **`unsigned`** , а **`unsigned`** можно использовать как краткую форму **`unsigned int`** . Типы перечислений ( **`enum`** ) также в большинстве случаев обрабатываются как целочисленные типы. К *типам с плавающей запятой* относятся **`float`** , **`double`** и **`long double`** . *Арифметические типы* включают все целочисленные типы и типы с плавающей запятой.

## <a name="see-also"></a>См. также

[Объявления и типы](../c-language/declarations-and-types.md)
