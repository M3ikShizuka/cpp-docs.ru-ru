---
description: 'Дополнительные сведения: перегрузка &lt; &lt; оператора для собственных классов'
title: Перегрузка оператора &lt;&lt; для собственных классов
ms.date: 11/04/2016
helpviewer_keywords:
- operator<<, overloading for your own classes
- operator <<, overloading for your own classes
ms.assetid: ad1d2c49-d84e-48a8-9c09-121f28b10bf0
ms.openlocfilehash: 206d6ccb50c7cb3706c66adeb6c1429a04775fc1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340844"
---
# <a name="overloading-the-ltlt-operator-for-your-own-classes"></a>Перегрузка оператора &lt;&lt; для собственных классов

Потоки ввода используют оператор вставки (`<<`) для стандартных типов. Оператор `<<` для собственных классов можно перегрузить.

## <a name="example"></a>Пример

Пример функции `write` показывает использование структуры `Date`. Даты хорошо подходят для класса C++, в котором члены данных (месяц, день и год) скрыты от просмотра. Поток вывода является логическим местом назначения для отображения такой структуры. Этот код отображает дату с помощью объекта `cout`:

```cpp
Date dt(1, 2, 92);

cout <<dt;
```

Чтобы `cout` принимал объект `Date` после оператора вставки, перегрузите оператор вставки для распознавания объектов `ostream` слева и `Date` справа. Перегруженная функция оператора `<<` затем должна быть объявлена как друг класса `Date`, он может получить доступ к личных данных в пределах `Date` объекта.

```cpp
// overload_date.cpp
// compile with: /EHsc
#include <iostream>
using namespace std;

class Date
{
    int mo, da, yr;
public:
    Date(int m, int d, int y)
    {
        mo = m; da = d; yr = y;
    }
    friend ostream& operator<<(ostream& os, const Date& dt);
};

ostream& operator<<(ostream& os, const Date& dt)
{
    os << dt.mo << '/' << dt.da << '/' << dt.yr;
    return os;
}

int main()
{
    Date dt(5, 6, 92);
    cout << dt;
}
```

```Output
5/6/92
```

## <a name="remarks"></a>Комментарии

Перегруженный оператор возвращает ссылку на исходный объект `ostream`, то есть вставки можно объединить:

```cpp
cout <<"The date is" <<dt <<flush;
```

## <a name="see-also"></a>См. также раздел

[Выходные потоки](../standard-library/output-streams.md)
