---
description: 'Дополнительные сведения о: &lt; ostream&gt;'
title: '&lt;ostream&gt;'
ms.date: 11/04/2016
f1_keywords:
- <ostream>
helpviewer_keywords:
- ostream header
ms.assetid: 90c3b6fb-57cd-4ae7-99b8-8512f24a67d2
ms.openlocfilehash: a31ffe801fca16e3b7fc1037c59613150e383933
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126433"
---
# <a name="ltostreamgt"></a>&lt;ostream&gt;

Определяет шаблон класса [basic_ostream](../standard-library/basic-ostream-class.md), который устраняет операции вставки для iostream. Заголовок также определяет несколько связанных манипуляторов. (Этот заголовок обычно включается автоматически при использовании других заголовков iostream. Его редко приходится включать напрямую.)

## <a name="syntax"></a>Синтаксис

```cpp
#include <ostream>
```

### <a name="typedefs"></a>Определения типов

|Имя типа|Описание|
|-|-|
|[ostream](../standard-library/ostream-typedefs.md#ostream)|Создает тип из `basic_ostream` , который специализируется на **`char`** и `char_traits` специализируется на **`char`** .|
|[wostream](../standard-library/ostream-typedefs.md#wostream)|Создает тип из `basic_ostream` , который специализируется на **`wchar_t`** и `char_traits` специализируется на **`wchar_t`** .|

### <a name="manipulators"></a>Манипуляторы

|Имя|Описание|
|-|-|
|[endl](../standard-library/ostream-functions.md#endl)|Завершает строку и очищает буфер.|
|[начинает](../standard-library/ostream-functions.md#ends)|Завершает строку.|
|[flush](../standard-library/ostream-functions.md#flush)|Очищает буфер.|
|[позиции](../standard-library/ostream-functions.md#swap)|Меняет местами значения левого параметра объекта `basic_ostream` со значениями правого параметра объекта `basic_ostream`.|

### <a name="operators"></a>Операторы

|Оператор|Описание|
|-|-|
|[Оператор<<](../standard-library/ostream-operators.md#op_lt_lt)|Записывает в поток различные типы.|

### <a name="classes"></a>Классы

|Класс|Описание|
|-|-|
|[basic_ostream](../standard-library/basic-ostream-class.md)|Шаблон класса описывает объект, управляющий вставкой элементов и закодированных объектов в буфер потока.|

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Программирование iostream](../standard-library/iostream-programming.md)\
[Соглашения iostream](../standard-library/iostreams-conventions.md)
