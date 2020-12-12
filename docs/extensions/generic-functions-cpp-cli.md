---
description: 'Дополнительные сведения: универсальные функции (C++/CLI)'
title: Универсальные функции (C++/CLI)
ms.date: 10/12/2018
ms.topic: reference
helpviewer_keywords:
- functions [C++], generic
- generic methods
- generics [C++], functions
- methods [C++], generic
- generic functions
ms.assetid: 8e409364-58f9-4360-b486-e7d555e0c218
ms.openlocfilehash: cd2c5390499e6858824fae7a3368afe6de8c6c56
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97301741"
---
# <a name="generic-functions-ccli"></a>Универсальные функции (C++/CLI)

Универсальная функция — это функция, объявляемая с параметрами типа. При ее вызове вместо параметров типа используются фактические типы.

## <a name="all-platforms"></a>Все платформы

### <a name="remarks"></a>Комментарии

Эта возможность применяется не для всех платформ.

## <a name="windows-runtime"></a>Среда выполнения Windows

### <a name="remarks"></a>Комментарии

В среде выполнения Windows эта функция языка не поддерживается.

### <a name="requirements"></a>Требования

Параметр компилятора: `/ZW`

## <a name="common-language-runtime"></a>Среда CLR

Универсальная функция — это функция, объявляемая с параметрами типа. При ее вызове вместо параметров типа используются фактические типы.

### <a name="syntax"></a>Синтаксис

```cpp
[attributes] [modifiers]
return-type identifier<type-parameter identifier(s)>
[type-parameter-constraints clauses]

([formal-parameters])
{function-body}
```

### <a name="parameters"></a>Параметры

*attributes*<br/>
(Необязательно) Дополнительные описательные данные. Дополнительные сведения об атрибутах и классах атрибутов см. в разделе "Атрибуты".

*модификаторы*<br/>
(Необязательно) Модификатор для функции, например static.  **`virtual`** не допускается, так как виртуальные методы могут быть неуниверсальными.

*Тип возвращаемого значения*<br/>
Тип, возвращаемый методом. Если тип возвращаемого значения — void, возвращаемое значение не требуется.

*identifier*<br/>
Имя функции.

*Идентификаторы type-parameter*<br/>
Разделенный запятыми список идентификаторов.

*formal-parameters*<br/>
(Необязательно) Список параметров.

*type-parameter-constraints-clauses*<br/>
Указывает ограничения для типов, которые могут использоваться в качестве аргументов типа, и имеет формат, определенный в статье [Constraints on Generic Type Parameters (C++/CLI)](constraints-on-generic-type-parameters-cpp-cli.md) (Ограничения параметров универсального типа в C++/CLI).

*тело функции*<br/>
Тело метода, который может ссылаться на идентификаторы параметров типа.

### <a name="remarks"></a>Комментарии

Универсальные функции — это функции, объявленные с параметром универсального типа. Они могут быть методами в классе или структуре или автономными функциями. В одном универсальном объявлении неявно объявляется семейство функций, отличающихся только подстановкой различных фактических типов вместо параметра универсального типа.

Конструкторы класса или структуры не могут объявляться с параметрами универсального типа.

При вызове параметр универсального типа заменяется фактическим типом. Фактический тип может быть явно указан в угловых скобках с использованием синтаксиса, аналогичного синтаксису вызова шаблонной функции. При вызове без параметров типа компилятор будет пытаться определить фактический тип по параметрам, указанным в вызове функции. Если определить заданный аргумент типа по используемым параметрам не удается, компилятор выдает ошибку.

### <a name="requirements"></a>Требования

Параметр компилятора: `/clr`

### <a name="examples"></a>Примеры

В следующем примере кода демонстрируется универсальная функция.

```cpp
// generics_generic_function_1.cpp
// compile with: /clr
generic <typename ItemType>
void G(int i) {}

ref struct A {
   generic <typename ItemType>
   void G(ItemType) {}

   generic <typename ItemType>
   static void H(int i) {}
};

int main() {
   A myObject;

   // generic function call
   myObject.G<int>(10);

   // generic function call with type parameters deduced
   myObject.G(10);

   // static generic function call
   A::H<int>(10);

   // global generic function call
   G<int>(10);
}
```

Универсальные функции могут перегружаться на основе сигнатуры или арности (количества параметров типа для функции). Они также могут перегружаться неуниверсальными функциями с таким же именем, если функции отличаются некоторыми параметрами типа. Например, могут перегружаться следующие функции:

```cpp
// generics_generic_function_2.cpp
// compile with: /clr /c
ref struct MyClass {
   void MyMythod(int i) {}

   generic <class T>
   void MyMythod(int i) {}

   generic <class T, class V>
   void MyMythod(int i) {}
};
```

В следующем примере используется универсальная функция, чтобы найти первый элемент массива. В примере объявляется класс `MyClass`, который наследуется от базового класса `MyBaseClass`. `MyClass` содержит универсальную функцию `MyFunction`, вызывающую другую универсальную функцию `MyBaseClassFunction` в базовом классе. В `main` универсальная функция `MyFunction` вызывается с использованием разных аргументов типа.

```cpp
// generics_generic_function_3.cpp
// compile with: /clr
using namespace System;

ref class MyBaseClass {
protected:
   generic <class ItemType>
   ItemType MyBaseClassFunction(ItemType item) {
      return item;
   }
};

ref class MyClass: public MyBaseClass {
public:
   generic <class ItemType>
   ItemType MyFunction(ItemType item) {
      return MyBaseClass::MyBaseClassFunction<ItemType>(item);
   }
};

int main() {
   MyClass^ myObj = gcnew MyClass();

   // Call MyFunction using an int.
   Console::WriteLine("My function returned an int: {0}",
                           myObj->MyFunction<int>(2003));

   // Call MyFunction using a string.
   Console::WriteLine("My function returned a string: {0}",
   myObj->MyFunction<String^>("Hello generic functions!"));
}
```

```Output
My function returned an int: 2003
My function returned a string: Hello generic functions!
```

## <a name="see-also"></a>См. также раздел

[Расширения компонентов для .NET и UWP](component-extensions-for-runtime-platforms.md)<br/>
[Универсальные шаблоны](generics-cpp-component-extensions.md)
