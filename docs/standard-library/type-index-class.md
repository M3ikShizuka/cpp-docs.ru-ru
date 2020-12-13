---
description: 'Дополнительные сведения о: type_index классе'
title: Класс type_index
ms.date: 11/04/2016
f1_keywords:
- typeindex/std::type_index
helpviewer_keywords:
- type_index class
ms.assetid: db366119-74cb-43e8-aacf-9679e561fa2f
ms.openlocfilehash: 4e9156420811d2712a5b9331d0ece0e7847103e9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142692"
---
# <a name="type_index-class"></a>Класс type_index

Класс `type_index` оборачивает указатель в [класс type_info](../cpp/type-info-class.md) для упрощения индексации такими объектами.

класс type_index {public: type_index (const type_info& тинфо); const char * Name () const; size_t hash_code () const; bool-оператор = = (const type_info& right) const; логический оператор! = (const type_info& right) const; логический оператор< (const type_info& right) const; логический оператор \<=(const type_info& right) const;
   bool operator> (const type_info& right) const; логический оператор>= (const type_info& right) const;};

Конструктор инициализирует `ptr` в `&tinfo`.

`name` возвращает `ptr->name()`.

`hash_code` возвращает `ptr->hash_code().`

`operator==` возвращает `*ptr == right.ptr`.

`operator!=` возвращает `!(*this == right)`.

`operator<` возвращает `*ptr->before(*right.ptr)`.

`operator<=` возвращает `!(right < *this).`

`operator>` возвращает `right < *this`.

`operator>=` возвращает `!(*this < right)`.

## <a name="see-also"></a>См. также раздел

[Сведения о типах времени выполнения](../cpp/run-time-type-information.md)\
[\<typeindex>](../standard-library/typeindex.md)
