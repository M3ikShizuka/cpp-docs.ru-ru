---
description: 'Дополнительные сведения о свойстве: Property (C++)'
title: property (C++)
ms.date: 11/04/2016
f1_keywords:
- property_cpp
helpviewer_keywords:
- property __declspec keyword
- __declspec keyword [C++], property
ms.assetid: f3b850ba-bf48-4df7-a1d6-8259d97309ce
ms.openlocfilehash: ed996ecadd16837af1e28b71bbedd9b4e3c1abaa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97299167"
---
# <a name="property-c"></a>property (C++)

**Блок, относящийся только к системам Microsoft**

Этот атрибут может применяться к нестатическим "виртуальным данным-членам" в определении класса или структуры. Компилятор обрабатывает эти "виртуальные данные-члены" как данные-член, заменяя ссылки вызовами функций.

## <a name="syntax"></a>Синтаксис

```
   __declspec( property( get=get_func_name ) ) declarator
   __declspec( property( put=put_func_name ) ) declarator
   __declspec( property( get=get_func_name, put=put_func_name ) ) declarator
```

## <a name="remarks"></a>Remarks

Когда компилятор видит элемент данных, объявленный с этим атрибутом, справа от оператора выбора члена ("**.**" или " **->** "), он преобразует операцию в `get` `put` функцию или, в зависимости от того, является ли такое выражение l-значением или r-value. В более сложных контекстах, таких как « `+=` », переписывание выполняется как, так `get` и `put` .

Этот атрибут также может использоваться при объявлении пустого массива в определении класса или структуры. Пример:

```cpp
__declspec(property(get=GetX, put=PutX)) int x[];
```

Приведенный выше оператор указывает, что `x[]` может использоваться с одним или несколькими индексами массива. В этом случае выражение `i=p->x[a][b]` будет преобразовано в `i=p->GetX(a, b)`, а выражение `p->x[a][b] = i` будет преобразовано в `p->PutX(a, b, i);`

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="example"></a>Пример

```cpp
// declspec_property.cpp
struct S {
   int i;
   void putprop(int j) {
      i = j;
   }

   int getprop() {
      return i;
   }

   __declspec(property(get = getprop, put = putprop)) int the_prop;
};

int main() {
   S s;
   s.the_prop = 5;
   return s.the_prop;
}
```

## <a name="see-also"></a>См. также раздел

[__declspec](../cpp/declspec.md)<br/>
[Ключевые слова](../cpp/keywords-cpp.md)
