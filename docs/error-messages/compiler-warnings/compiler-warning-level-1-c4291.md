---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4291'
title: Предупреждение компилятора (уровень 1) C4291
ms.date: 11/04/2016
f1_keywords:
- C4291
helpviewer_keywords:
- C4291
ms.assetid: c2b95dea-38f2-4609-9104-707c30798da4
ms.openlocfilehash: 190fbb1ed91c5524dcd83a0a02a0b0280e264891
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340116"
---
# <a name="compiler-warning-level-1-c4291"></a>Предупреждение компилятора (уровень 1) C4291

"объявление": не найден соответствующий оператор DELETE; память не будет освобождена, если при инициализации возникает исключение

Используется размещение [New](../../cpp/new-operator-cpp.md) , для которого не существует [удаления](../../cpp/delete-operator-cpp.md)размещения.

При выделении памяти для объекта с оператором **`new`** вызывается конструктор объекта. Если конструктор создает исключение, то память, выделенная для объекта, должна быть освобождена. Это не может быть выполнено, если не **`delete`** существует функции оператора, соответствующей оператору **`new`** .

Если вы используете оператор **`new`** без дополнительных аргументов и компилируете параметры [/GX](../../build/reference/gx-enable-exception-handling.md), [/EHs](../../build/reference/eh-exception-handling-model.md)или/EHA для включения обработки исключений, компилятор создаст код для вызова оператора, **`delete`** Если конструктор выдаст исключение.

Если вы используете форму размещения **`new`** оператора (форма с аргументами в дополнение к размеру выделения) и конструктор объекта создает исключение, компилятор по-прежнему будет создавать код для вызова оператора, **`delete`** но это делается только в том случае, если существует форма оператора размещения **`delete`** , соответствующая форме оператора **`new`** , который выделил память. Пример:

```cpp
// C4291.cpp
// compile with: /EHsc /W1
#include <malloc.h>

class CList
{
public:
   CList(int)
   {
      throw "Fail!";
   }
};

void* operator new(size_t size, char* pszFilename, int nLine)
{
   return malloc(size);
}

int main(void)
{
   try
   {
      // This will call ::operator new(unsigned int) to allocate heap
      // memory. Heap memory pointed to by pList1 will automatically be
      // deallocated by a call to ::operator delete(void*) when
      // CList::CList(int) throws an exception.
      CList* pList1 = new CList(10);
   }
   catch (...)
   {
   }

   try
   {
      // This will call the overloaded ::operator new(size_t, char*, int)
      // to allocate heap memory. When CList::CList(int) throws an
      // exception, ::operator delete(void*, char*, int) should be called
      // to deallocate the memory pointed to by pList2. Since
      // ::operator delete(void*, char*, int) has not been implemented,
      // memory will be leaked when the deallocation cannot occur.
      CList* pList2 = new(__FILE__, __LINE__) CList(20);   // C4291
   }
   catch (...)
   {
   }
}
```

Приведенный выше пример приводит к возникновению предупреждения C4291, так как не **`delete`** определена форма оператора, которая соответствует форме оператора размещения **`new`** . Чтобы решить эту проблему, вставьте следующий код выше **Main**. Обратите внимание, что все параметры перегруженной **`delete`** функции оператора соответствуют параметрам перегруженного оператора **`new`** , за исключением первого параметра.

```cpp
void operator delete(void* pMem, char* pszFilename, int nLine)
{
   free(pMem);
}
```
