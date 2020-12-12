---
description: 'Дополнительные сведения: экспорт'
title: Export (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.export
helpviewer_keywords:
- export attribute
ms.assetid: 70b3e848-fad6-4e09-8c72-be60ca72a4df
ms.openlocfilehash: 40c802f906d62d72be2c3126159b089c4d24d5b8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97236299"
---
# <a name="export"></a>экспорт

Приводит к размещению структуры данных в IDL-файле.

## <a name="syntax"></a>Синтаксис

```cpp
[export]
```

## <a name="remarks"></a>Remarks

**`[export]`** Атрибут C++ заставляет разместить структуру данных в IDL-файле и затем быть доступной в библиотеке типов в двоичном совместимом формате, который делает его доступным для использования с любым языком.

Атрибут нельзя применить **`[export]`** к классу, даже если он содержит только открытые члены (эквивалент типа **`struct`** ).

Если вы экспортируете безымянное имя **`enum`** или **`struct`** , ему присваивается имя, начинающееся с **__unnamed**<em>x</em>, где *x* — это порядковый номер.

Определение типов, допустимых для экспорта, — это базовые типы, структуры, объединения, перечисления или идентификаторы типов.  [`typedef`](/windows/win32/Midl/typedef)Дополнительные сведения см. в разделе.

## <a name="example"></a>Пример

В следующем коде показано, как использовать **`[export]`** атрибут:

```cpp
// cpp_attr_ref_export.cpp
// compile with: /LD
[module(name="MyLibrary")];

[export]
struct MyStruct {
   int i;
};
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**`union`**,,, **`typedef`** **`enum`** **`struct`** или **`interface`**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты компилятора](compiler-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)
