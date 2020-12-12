---
description: 'Дополнительные сведения: изменяемые элементы данных (C++)'
title: Изменяемые члены данных (C++)
ms.date: 11/04/2016
f1_keywords:
- mutable_cpp
helpviewer_keywords:
- mutable keyword [C++]
ms.assetid: ebe89746-3d36-43a8-8d69-f426af23f551
ms.openlocfilehash: a288b382b456fa313c49832bd2d13aaceb269be9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313818"
---
# <a name="mutable-data-members-c"></a>Изменяемые члены данных (C++)

Это ключевое слово может применяться только к данным-членам класса, которые не являются статическими или константами. Если объявлен элемент данных **`mutable`** , ему допустимо присвоить значение этому элементу данных из **`const`** функции-члена.

## <a name="syntax"></a>Синтаксис

```
mutable member-variable-declaration;
```

## <a name="remarks"></a>Remarks

Например, следующий код будет компилироваться без ошибок, поскольку `m_accessCount` объявлен как **`mutable`** , и поэтому может быть изменен, `GetFlag` даже если `GetFlag` является константной функцией-членом.

```cpp
// mutable.cpp
class X
{
public:
   bool GetFlag() const
   {
      m_accessCount++;
      return m_flag;
   }
private:
   bool m_flag;
   mutable int m_accessCount;
};

int main()
{
}
```

## <a name="see-also"></a>См. также раздел

[Ключевые слова](../cpp/keywords-cpp.md)
