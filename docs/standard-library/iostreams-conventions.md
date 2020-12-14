---
description: Дополнительные сведения о соглашениях iostream
title: Соглашения iostreams
ms.date: 11/04/2016
helpviewer_keywords:
- iostream header
- C++ Standard Library, iostreams
ms.assetid: 9fe5ded0-37a1-48d1-9671-c81ffc4760ad
ms.openlocfilehash: 3676c6aa14a5ebac1d39ed50821449caa7313e40
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231398"
---
# <a name="iostreams-conventions"></a>Соглашения iostreams

Заголовки iostreams поддерживают преобразования между текстом и закодированными формами, а также ввод и вывод во внешние файлы.

[\<fstream>](../standard-library/fstream.md)\
[\<iomanip>](../standard-library/iomanip.md)\
[\<ios>](../standard-library/ios.md)\
[\<iosfwd>](../standard-library/iosfwd.md)\
[\<iostream>](../standard-library/iostream.md)\
[\<istream>](../standard-library/istream.md)\
[\<ostream>](../standard-library/ostream.md)\
[\<sstream>](../standard-library/sstream.md)\
[\<streambuf>](../standard-library/streambuf.md)\
[\<strstream>](../standard-library/strstream.md)

Простейшее использование iostream подразумевает только включение заголовка [\<iostream>](../standard-library/iostream.md) . После этого можно извлечь значения из [cin](../standard-library/iostream.md#cin) или [wcin](../standard-library/iostream.md#wcin) для чтения из стандартного ввода. Правила для этого приведены в описании класса [basic_istream](../standard-library/basic-istream-class.md). Вы также можете вставить значения в [cout](../standard-library/iostream.md#cout) или [wcout](../standard-library/iostream.md#wcout) для записи в стандартный вывод. Правила для этого приведены в описании класса [basic_ostream](../standard-library/basic-ostream-class.md). Контроль формата для средств извлечения и средств вставки выполняется с помощью класса [класс basic_ios](../standard-library/basic-ios-class.md). Обработка этой информации о формате извлекающих и вставляющих объектов относится к области нескольких манипуляторов.

Вы можете выполнять одни и те же операции iostream для файлов, открываемых по имени, используя классы, объявленные в [\<fstream>](../standard-library/fstream.md) . Чтобы выполнить преобразование между iostream и объектами класса [Basic_string класса](../standard-library/basic-string-class.md), используйте классы, объявленные в [\<sstream>](../standard-library/sstream.md) . Чтобы сделать то же самое с строками C, используйте классы, объявленные в [\<strstream>](../standard-library/strstream.md) .

Остальные заголовки обеспечивают вспомогательные службы, обычно интересные только самым опытным пользователям классов iostreams.

## <a name="see-also"></a>См. также раздел

[Общие сведения о стандартной библиотеке C++](../standard-library/cpp-standard-library-overview.md)\
[Программирование iostream](../standard-library/iostream-programming.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
