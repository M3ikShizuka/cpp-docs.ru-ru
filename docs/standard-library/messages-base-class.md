---
description: 'Дополнительные сведения о: messages_base классе'
title: Класс messages_base
ms.date: 11/04/2016
f1_keywords:
- xlocmes/std::messages_base
helpviewer_keywords:
- messages_base class
ms.assetid: 9aad38c6-4c13-445d-b096-364bd0836efb
ms.openlocfilehash: 45ea81b02bd15011c9f98b9364ea9918e248692a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230592"
---
# <a name="messages_base-class"></a>Класс messages_base

Базовый класс описывает **`int`** тип для каталога сообщений.

## <a name="syntax"></a>Синтаксис

```cpp
struct messages_base : locale::facet {
    typedef int catalog;
    explicit messages_base(size_t _Refs = 0)
};
```

## <a name="remarks"></a>Remarks

Каталог типов является синонимом типа **`int`** , который описывает возможные возвращаемые значения из сообщений:: [do_open](../standard-library/messages-class.md#do_open).

## <a name="requirements"></a>Требования

**Заголовок:**\<locale>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
