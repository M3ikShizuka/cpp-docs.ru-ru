---
description: Дополнительные сведения об pragma директиве init_seg в Microsoft C/C++
title: init_seg pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.init_seg
- init_seg_CPP
helpviewer_keywords:
- pragma, init_seg
- init_seg pragma
- data segment initializing [C++]
no-loc:
- pragma
ms.openlocfilehash: 77ca6f2454ad18c8adcefcddc4cf1f9c0d4f4532
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713588"
---
# <a name="init_seg-no-locpragma"></a>`init_seg` pragma

**Блок, относящийся только к языку C++**

Определяет ключевое слово или раздел кода, влияющие на порядок выполнения кода запуска.

## <a name="syntax"></a>Синтаксис

> **`#pragma init_seg(`** { **`compiler`** | **`lib`** | **`user`** | "*section-name*" [ **`,`** *Func-Name* ]} **`)`**

## <a name="remarks"></a>Примечания

Термины *сегмент* и *раздел* имеют одинаковое значение в этой статье.

Поскольку код иногда требуется для инициализации глобальных статических объектов, необходимо указать время создания объектов. В частности, важно использовать **`init_seg`** pragma в библиотеках динамической компоновки (DLL) или в библиотеках, требующих инициализации.

**`init_seg`** pragma Доступны следующие параметры:

**`compiler`**\
Зарезервирован для инициализации библиотеки времени выполнения Microsoft C. Объекты в этой группе создаются первыми.

**`lib`**\
Доступен для инициализаций поставщиков сторонних библиотек классов. Объекты в этой группе создаются после тех, которые помечены как **`compiler`** , но перед другими.

**`user`**\
Доступен для любого пользователя. Объекты в этой группе создаются последними.

*имя раздела*\
Позволяет явно определить раздел инициализации. Объекты в указанном пользователем *разделе Name* не создаются неявно. Однако их адреса помещаются в раздел с именем *section-name*.

*Имя раздела* , которое вы присваиваете, будет содержать указатели на вспомогательные функции, которые будут формировать глобальные объекты, объявленные после pragma в этом модуле.

Список имен, которые не следует использовать при создании раздела, см. в разделе [`/SECTION`](../build/reference/section-specify-section-attributes.md) .

*Func-Name*\
Определяет функцию, вызываемую вместо функции `atexit` при выходе из программы. Эта вспомогательная функция также вызывает [`atexit`](../c-runtime-library/reference/atexit.md) с указателем на деструктор для глобального объекта. Если в форме указан идентификатор функции pragma ,

```cpp
int __cdecl myexit (void (__cdecl *pf)(void))
```

то вместо функции `atexit` библиотеки времени выполнения C будет вызываться пользовательская функция. Он позволяет создать список деструкторов, которые будут вызываться, когда все будет готово к уничтожению объектов.

Если требуется отложить инициализацию (например, в библиотеке DLL), можно явно указать имя раздела. Затем код должен вызывать конструкторы для каждого статического объекта.

Идентификатор для замены функции `atexit` не заключается в кавычки.

Объекты по-прежнему будут помещены в разделы, определенные другими `XXX_seg` pragma директивами.

Объекты, объявленные в модуле, не инициализируются автоматически с помощью среды выполнения C. Код должен выполнять инициализацию.

По умолчанию разделы `init_seg` предназначены только для чтения. Если имя раздела — `.CRT` , компилятор автоматически изменяет атрибут на только чтение, даже если он помечен как Read, Write.

В записи преобразования нельзя указывать **`init_seg`** больше одного раза.

Даже если у вашего объекта нет пользовательского конструктора, который явно определен в коде, компилятор может создать его. Например, он может создать один для привязки указателей v-table. При необходимости код вызывает конструктор, созданный компилятором.

## <a name="example"></a>Пример

```cpp
// pragma_directive_init_seg.cpp
#include <stdio.h>
#pragma warning(disable : 4075)

typedef void (__cdecl *PF)(void);
int cxpf = 0;   // number of destructors we need to call
PF pfx[200];    // pointers to destructors.

int myexit (PF pf) {
   pfx[cxpf++] = pf;
   return 0;
}

struct A {
   A() { puts("A()"); }
   ~A() { puts("~A()"); }
};

// ctor & dtor called by CRT startup code
// because this is before the pragma init_seg
A aaaa;

// The order here is important.
// Section names must be 8 characters or less.
// The sections with the same name before the $
// are merged into one section. The order that
// they are merged is determined by sorting
// the characters after the $.
// InitSegStart and InitSegEnd are used to set
// boundaries so we can find the real functions
// that we need to call for initialization.

#pragma section(".mine$a", read)
__declspec(allocate(".mine$a")) const PF InitSegStart = (PF)1;

#pragma section(".mine$z",read)
__declspec(allocate(".mine$z")) const PF InitSegEnd = (PF)1;

// The comparison for 0 is important.
// For now, each section is 256 bytes. When they
// are merged, they are padded with zeros. You
// can't depend on the section being 256 bytes, but
// you can depend on it being padded with zeros.

void InitializeObjects () {
   const PF *x = &InitSegStart;
   for (++x ; x < &InitSegEnd ; ++x)
      if (*x) (*x)();
}

void DestroyObjects () {
   while (cxpf>0) {
      --cxpf;
      (pfx[cxpf])();
   }
}

// by default, goes into a read only section
#pragma init_seg(".mine$m", myexit)

A bbbb;
A cccc;

int main () {
   InitializeObjects();
   DestroyObjects();
}
```

```Output
A()
A()
A()
~A()
~A()
~A()
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
