---
title: 'Оператор разрешения области: `::`'
description: Узнайте, как работает оператор разрешения области `::` в стандартном C++.
ms.date: 12/06/2020
f1_keywords:
- '::'
helpviewer_keywords:
- scope, scope resolution operator
- operators [C++], scope resolution
- scope resolution operator
- ':: operator'
ms.openlocfilehash: ff774d9fcca9f68cb2925af82c55ef438ab4d71a
ms.sourcegitcommit: 7b131db4ed39bddb4a456ebea402f47c5cbd69d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/07/2020
ms.locfileid: "96776535"
---
# <a name="scope-resolution-operator-"></a>Оператор разрешения области: `::`

Оператор разрешения области **`::`** используется для идентификации и устранения неоднозначности идентификаторов, используемых в разных областях. Дополнительные сведения об области действия см. в разделе [Scope](../cpp/scope-visual-cpp.md).

## <a name="syntax"></a>Синтаксис

> *`qualified-id`*:\
> &emsp; *`nested-name-specifier`* **`template`** <sub>необ.</sub> *`unqualified-id`*

> *`nested-name-specifier`*:\
> &emsp;**`::`**\
> &emsp;*`type-name`* **`::`**\
> &emsp;*`namespace-name`* **`::`**\
> &emsp;*`decltype-specifier`* **`::`**\
> &emsp;*`nested-name-specifier`* *`identifier`* **`::`**\
> &emsp;*`nested-name-specifier`***`template`** <sub>неявное согласие</sub> *`simple-template-id`***`::`**

> *`unqualified-id`*:\
> &emsp;*`identifier`*\
> &emsp;*`operator-function-id`*\
> &emsp;*`conversion-function-id`*\
> &emsp;*`literal-operator-id`*\
> &emsp;**`~`** *`type-name`*\
> &emsp;**`~`** *`decltype-specifier`*\
> &emsp;*`template-id`*

## <a name="remarks"></a>Комментарии

`identifier` может быть переменной, функцией или значением перечисления.

## <a name="use--for-classes-and-namespaces"></a>Использование `::` для классов и пространств имен

В следующем примере показано, каким образом оператор разрешения области используется с пространствами имен и классами:

```cpp
namespace NamespaceA{
    int x;
    class ClassA {
    public:
        int x;
    };
}

int main() {

    // A namespace name used to disambiguate
    NamespaceA::x = 1;

    // A class name used to disambiguate
    NamespaceA::ClassA a1;
    a1.x = 2;
}
```

Оператор разрешения области без квалификатора области применяется к глобальному пространству имен.

```cpp
namespace NamespaceA{
    int x;
}

int x;

int main() {
    int x;

    // the x in main()
    x = 0;
    // The x in the global namespace
    ::x = 1;

    // The x in the A namespace
    NamespaceA::x = 2;
}
```

Оператор разрешения области можно использовать для определения члена **`namespace`** или для определения пространства имен, которое определяет пространство имен члена в **`using`** директиве. В приведенном ниже примере можно использовать `NamespaceC` для уточнения `ClassB` , даже если `ClassB` он был объявлен в пространстве имен `NamespaceB` , так как `NamespaceB` был назначен в `NamespaceC` **`using`** директиве.

```cpp
namespace NamespaceB {
    class ClassB {
    public:
        int x;
    };
}

namespace NamespaceC{
    using namespace NamespaceB;
}

int main() {
    NamespaceB::ClassB b_b;
    NamespaceC::ClassB c_b;

    b_b.x = 3;
    c_b.x = 4;
}
```

Можно использовать цепочки операторов разрешения области. В следующем примере `NamespaceD::NamespaceD1` определяет вложенное пространство имен `NamespaceD1`, а `NamespaceE::ClassE::ClassE1` определяет вложенный класс `ClassE1`.

```cpp
namespace NamespaceD{
    namespace NamespaceD1{
        int x;
    }
}

namespace NamespaceE{
    class ClassE{
    public:
        class ClassE1{
        public:
            int x;
        };
    };
}

int main() {
    NamespaceD:: NamespaceD1::x = 6;
    NamespaceE::ClassE::ClassE1 e1;
    e1.x = 7  ;
}
```

## <a name="use--for-static-members"></a>Использовать `::` для статических членов

Оператор разрешения области необходимо использовать для вызова статических членов класса.

```cpp
class ClassG {
public:
    static int get_x() { return x;}
    static int x;
};

int ClassG::x = 6;

int main() {

    int gx1 = ClassG::x;
    int gx2 = ClassG::get_x();
}
```

## <a name="use--for-scoped-enumerations"></a>Используется `::` для перечислений с заданной областью

Оператор разрешения с заданной областью также используется со значениями [объявлений перечисления](../cpp/enumerations-cpp.md)в области перечисления, как показано в следующем примере:

```cpp
enum class EnumA{
    First,
    Second,
    Third
};

int main() {
    EnumA enum_value = EnumA::First;
}
```

## <a name="see-also"></a>См. также раздел

[Встроенные операторы, приоритет и ассоциативность C++](../cpp/cpp-built-in-operators-precedence-and-associativity.md)<br/>
[Пространства имен](../cpp/namespaces-cpp.md)
