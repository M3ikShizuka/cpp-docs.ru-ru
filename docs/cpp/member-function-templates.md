---
description: 'Дополнительные сведения: шаблоны функций элементов'
title: Шаблоны функций-членов
ms.date: 11/04/2016
helpviewer_keywords:
- function templates, member functions
ms.assetid: 83d51835-6a27-40ed-997c-7d90dc9182d8
ms.openlocfilehash: ebeaab90c1ea21e70433fd969e7ee8185b5dcd22
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97161693"
---
# <a name="member-function-templates"></a>Шаблоны функций-членов

Шаблон элементов терминов относится как к шаблонам функций-членов, так и к шаблонам вложенных классов. Шаблоны функций-членов — это функции-шаблоны, являющиеся членами класса или шаблона класса.

Функции-члены могут являться функциями-шаблонами в нескольких контекстах. Все функции шаблонов классов являются общими, однако они не являются шаблонами элементов или шаблонами функций-членов. Если такие функции-члены принимают собственные аргументы шаблона, они считаются шаблонами функций-членов.

## <a name="example-declare-member-function-templates"></a>Пример. объявление шаблонов функций элементов

Шаблоны функции-члена нешаблонных или шаблонных классов объявляются в виде шаблонов функций с собственными шаблонными параметрами.

```cpp
// member_function_templates.cpp
struct X
{
   template <class T> void mf(T* t) {}
};

int main()
{
   int i;
   X* x = new X();
   x->mf(&i);
}
```

## <a name="example-member-function-template-of-template-class"></a>Пример: шаблон функции члена класса шаблона

В следующем примере показан шаблон функции-члена шаблонного класса.

```cpp
// member_function_templates2.cpp
template<typename T>
class X
{
public:
   template<typename U>
   void mf(const U &u)
   {
   }
};

int main()
{
}
```

## <a name="example-define-member-templates-outside-class"></a>Пример: Определение шаблонов элементов за пределами класса

```cpp
// defining_member_templates_outside_class.cpp
template<typename T>
class X
{
public:
   template<typename U>
   void mf(const U &u);
};

template<typename T> template <typename U>
void X<T>::mf(const U &u)
{
}

int main()
{
}
```

## <a name="example-templated-user-defined-conversion"></a>Пример. шаблонное определяемое пользователем преобразование

Локальные классы не могут иметь шаблоны элементов.

Функции шаблонов-элементов не могут быть виртуальными функциями или переопределять виртуальные функции из базового класса, если они объявлены с тем же именем, что и виртуальная функция базового класса.

В следующем примере показано определяемое пользователем преобразование с помощью шаблона:

```cpp
// templated_user_defined_conversions.cpp
template <class T>
struct S
{
   template <class U> operator S<U>()
   {
      return S<U>();
   }
};

int main()
{
   S<int> s1;
   S<long> s2 = s1;  // Convert s1 using UDC and copy constructs S<long>.
}
```

## <a name="see-also"></a>См. также раздел

[Шаблоны функций](../cpp/function-templates.md)
