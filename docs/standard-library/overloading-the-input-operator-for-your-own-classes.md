---
description: 'Дополнительные сведения: перегрузка &gt; &gt; оператора для собственных классов'
title: Перегрузка оператора &gt;&gt; для собственных классов
ms.date: 11/04/2016
helpviewer_keywords:
- operator>>
- operator>>, overloading for your own classes
- operator >>, overloading for your own classes
ms.assetid: 40dab4e0-3f97-4745-9cc8-b86e740fa246
ms.openlocfilehash: 4de7c16dd1c42f85f169da50f11a514eb245b47c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340857"
---
# <a name="overloading-the-gtgt-operator-for-your-own-classes"></a>Перегрузка оператора &gt;&gt; для собственных классов

Потоки ввода используют оператор извлечения (`>>`) для стандартных типов. Можно написать аналогичные операторы извлечения для собственных типов; успех зависит от правильности использования пустого пространства.

Ниже приведен пример оператора извлечения для класса `Date`, представленного выше.

```cpp
istream& operator>> (istream& is, Date& dt)
{
    is>> dt.mo>> dt.da>> dt.yr;
    return is;
}
```

## <a name="see-also"></a>См. также раздел

[Входные потоки](../standard-library/input-streams.md)
