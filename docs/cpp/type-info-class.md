---
description: 'Дополнительные сведения о: type_info классе'
title: Класс type_info
ms.date: 11/04/2016
f1_keywords:
- type_info
helpviewer_keywords:
- class type_info
- type_info class
ms.assetid: 894ddda2-7de4-4da3-9404-d2c74e356c16
ms.openlocfilehash: 6be4d6774842ad015b34e771455026ca27e6539b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295319"
---
# <a name="type_info-class"></a>Класс type_info

Класс **type_info** описывает сведения о типах, созданные в программе компилятором. Объекты этого класса эффективно сохраняют указатель на имя для типа. Класс **type_info** также хранит закодированное значение, пригодное для сравнения двух типов на равенство или порядок сортировки. Правила кодирования и последовательность размещения типов не указаны и могут различаться в разных программах.

`<typeinfo>`Для использования класса **type_info** должен быть добавлен файл заголовка. Интерфейс для класса **type_info** :

```cpp
class type_info {
public:
    type_info(const type_info& rhs) = delete; // cannot be copied
    virtual ~type_info();
    size_t hash_code() const;
    _CRTIMP_PURE bool operator==(const type_info& rhs) const;
    type_info& operator=(const type_info& rhs) = delete; // cannot be copied
    _CRTIMP_PURE bool operator!=(const type_info& rhs) const;
    _CRTIMP_PURE int before(const type_info& rhs) const;
    size_t hash_code() const noexcept;
    _CRTIMP_PURE const char* name() const;
    _CRTIMP_PURE const char* raw_name() const;
};
```

Нельзя напрямую создавать экземпляры объектов класса **type_info** , так как класс имеет только закрытый конструктор копии. Единственный способ создать (временный) объект **type_info** — использовать оператор [typeid](../cpp/typeid-operator.md) . Поскольку оператор присваивания также является закрытым, нельзя копировать или назначать объекты класса **type_info**.

`type_info::hash_code` определяет хэш-функцию, подходящую для сопоставления значений типа **typeInfo** с распределением значений индекса.

Операторы `==` и `!=` могут использоваться для сравнения на равенство и неравенство с другими **type_info** объектами соответственно.

Нет связи между порядком размещения типов и отношениями наследования. Используйте `type_info::before` функцию члена для определения порядка следования типов. Нет никакой гарантии, что `type_info::before` будет давать тот же результат в различных программах или даже в разных запусках одной программы. Таким образом, `type_info::before` аналогичен `(&)` оператору взятия адреса.

`type_info::name`Функция-член возвращает `const char*` в строку, завершающуюся нулем, представляющую понятное имя типа. Указываемая память кэшируется. Ее никогда не следует освобождать напрямую.

`type_info::raw_name`Функция-член возвращает `const char*` в строку, завершающуюся нулем, представляющую декорированное имя типа объекта. Имя фактически хранится в оформленном виде с целью экономии пространства. Следовательно, эта функция работает быстрее, чем `type_info::name` потому, что ей не нужно разменять имя. Строка, возвращаемая `type_info::raw_name` функцией, полезна в операциях сравнения, но недоступна для чтения. Если требуется доступная для человека строка, используйте `type_info::name` вместо нее функцию.

Сведения о типе для полиморфизма создаются только в том случае, если указан параметр компилятора [/GR (Enable Run-Time Type Information)](../build/reference/gr-enable-run-time-type-information.md) .

## <a name="see-also"></a>См. также раздел

[Сведения о типах среды выполнения](../cpp/run-time-type-information.md)
