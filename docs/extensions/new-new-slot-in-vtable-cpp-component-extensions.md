---
description: 'Дополнительные сведения: New (новый слот в vtable) (C++/CLI и C++/CX)'
title: new (новый слот в vtable) (C++/CLI и C++/CX)
ms.date: 10/12/2018
ms.topic: reference
helpviewer_keywords:
- new keyword [C++]
ms.assetid: 1a9a5704-f02f-46ae-ad65-f0f2b6dbabc3
ms.openlocfilehash: ccc6adbd29eca82b44d34b981803a88332a8784a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257683"
---
# <a name="new-new-slot-in-vtable--ccli-and-ccx"></a>new (новый слот в vtable) (C++/CLI и C++/CX)

**`new`** Ключевое слово указывает, что виртуальный член получит новый слот в таблице vtable.

## <a name="all-runtimes"></a>Все среды выполнения

(Отсутствуют комментарии для этой возможности языка, которая применяется во всех средах выполнения.)

## <a name="windows-runtime"></a>Среда выполнения Windows

Не поддерживается в среде выполнения Windows.

## <a name="common-language-runtime"></a>Среда CLR

### <a name="remarks"></a>Комментарии

При `/clr` компиляции **`new`** указывает, что виртуальный член получит новый слот в таблице vtable; эта функция не переопределяет метод базового класса.

**`new`** вызывает Добавление модификатора NewSlot к IL для функции.  Дополнительные сведения о newslot см. в эти статьях:

- <xref:System.Reflection.MethodInfo.GetBaseDefinition?displayProperty=nameWithType>

- <xref:System.Reflection.MethodAttributes?displayProperty=nameWithType>

### <a name="requirements"></a>Требования

Параметр компилятора: `/clr`

### <a name="examples"></a>Примеры

В следующем примере показан результат **`new`** .

```cpp
// newslot.cpp
// compile with: /clr
ref class C {
public:
   virtual void f() {
      System::Console::WriteLine("C::f() called");
   }

   virtual void g() {
      System::Console::WriteLine("C::g() called");
   }
};

ref class D : public C {
public:
   virtual void f() new {
      System::Console::WriteLine("D::f() called");
   }

   virtual void g() override {
      System::Console::WriteLine("D::g() called");
   }
};

ref class E : public D {
public:
   virtual void f() override {
      System::Console::WriteLine("E::f() called");
   }
};

int main() {
   D^ d = gcnew D;
   C^ c = gcnew D;

   c->f();   // calls C::f
   d->f();   // calls D::f

   c->g();   // calls D::g
   d->g();   // calls D::g

   D ^ e = gcnew E;
   e->f();   // calls E::f
}
```

```Output
C::f() called

D::f() called

D::g() called

D::g() called

E::f() called
```

## <a name="see-also"></a>См. также раздел

[Расширения компонентов для .NET и UWP](component-extensions-for-runtime-platforms.md)<br/>
[Спецификаторы переопределения](override-specifiers-cpp-component-extensions.md)
