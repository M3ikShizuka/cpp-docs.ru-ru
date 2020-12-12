---
description: 'Дополнительные сведения: потоки ввода-вывода'
title: Input-Outputные потоки
ms.date: 11/04/2016
helpviewer_keywords:
- I/O [C++], stream
- stream I/O
ms.assetid: 21a97566-91a7-42d6-b2f8-a4c16bc926f1
ms.openlocfilehash: fd261bfdac5b9ce95b04430e9d77c6bd1df56c7d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231645"
---
# <a name="inputoutput-streams"></a>Потоки ввода/вывода

`basic_iostream`, который определен в файле заголовка \<istream> , является шаблоном класса для объектов, обрабатывающих входные и выходные потоки ввода-вывода на основе символов.

Существуют два определения типов, которые определяют специализации для отдельных символов `basic_iostream` и могут облегчить чтение кода: `iostream` (не путать с файлом заголовка \<iostream> ) — это поток ввода-вывода, основанный на `basic_iostream<char>` `wiostream` . — это поток ввода-вывода, основанный на `basic_iostream<wchar_t>` .

Дополнительные сведения см. в разделах [Класс basic_iostream](../standard-library/basic-iostream-class.md), [iostream](../standard-library/basic-iostream-class.md) и [wiostream](../standard-library/basic-iostream-class.md).

Производным из `basic_iostream` является шаблон класса `basic_fstream`, который используется для потоковой передачи символьных данных в файлы и из них.

Также имеются определения типов, которые предоставляют специальные для символов специализации для `basic_fstream`. Они представляют собой `fstream` поток файлового ввода-вывода, основанный на **`char`** , и `wfstream` , который является потоком файлового ввода-вывода, основанным на **`wchar_t`** . Дополнительные сведения см. в разделах [Класс basic_fstream](../standard-library/basic-fstream-class.md), [fstream](../standard-library/basic-fstream-class.md) и [wfstream](../standard-library/basic-fstream-class.md). Использование этих определений типов требует включения файла заголовка \<fstream> .

> [!NOTE]
> Если объект `basic_fstream` используется для выполнения файлового ввода-вывода, хотя базовый буфер содержит отдельно назначенные позиции для чтения и записи, текущие позиции ввода и вывода связываются друг с другом, поэтому, чтение некоторых данных перемещает позицию вывода.

Шаблон класса `basic_stringstream` и его общая специализация `stringstream` часто используются для работы с объектами потока ввода-вывода для вставки и извлечения символьных данных. Дополнительные сведения см. в разделе [Класс basic_stringstream](../standard-library/basic-stringstream-class.md).

## <a name="see-also"></a>См. также раздел

[StringStream](../standard-library/basic-stringstream-class.md)\
[Класс basic_stringstream](../standard-library/basic-stringstream-class.md)\
[\<sstream>](../standard-library/sstream.md)\
[Программирование iostream](../standard-library/iostream-programming.md)\
[Стандартная библиотека C++](../standard-library/cpp-standard-library-reference.md)
