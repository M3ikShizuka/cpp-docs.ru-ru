---
description: 'Дополнительные сведения о: noreturn'
title: noreturn
ms.date: 11/04/2016
f1_keywords:
- noreturn_cpp
helpviewer_keywords:
- __declspec keyword [C++], noreturn
- noreturn __declspec keyword
ms.assetid: 9c6517e5-22d7-4051-9974-3d2200ae4d1d
ms.openlocfilehash: 829f8cc2d81ae1b9f55024442f1a38b495d54896
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97195363"
---
# <a name="noreturn"></a>noreturn

**Блок, относящийся только к системам Microsoft**

Этот **`__declspec`** атрибут сообщает компилятору, что функция не возвращает значение. Как следствие, компилятор знает, что код, следующий за вызовом **`__declspec(noreturn)`** функции, недоступен.

Если компилятор обнаруживает функцию с путем элемента управления, которая не возвращает значение, он создает предупреждение (C4715) или сообщение об ошибке (C2202). Если путь к элементу управления недоступен из-за функции, которая никогда не возвращает, можно использовать, **`__declspec(noreturn)`** чтобы предотвратить это предупреждение или ошибку.

> [!NOTE]
> Добавление **`__declspec(noreturn)`** в функцию, которая должна возвращать значение, может привести к неопределенному поведению.

## <a name="example"></a>Пример

В следующем примере **`else`** предложение не содержит оператор return.  Объявление `fatal` как **`__declspec(noreturn)`** не позволяет избежать сообщения об ошибке или предупреждении.

```cpp
// noreturn2.cpp
__declspec(noreturn) extern void fatal () {}

int main() {
   if(1)
     return 1;
   else if(0)
     return 0;
   else
     fatal();
}
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[__declspec](../cpp/declspec.md)<br/>
[Ключевые слова](../cpp/keywords-cpp.md)
