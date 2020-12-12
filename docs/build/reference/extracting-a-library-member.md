---
description: 'Дополнительные сведения: извлечение элемента библиотеки'
title: Извлечение члена библиотеки
ms.date: 11/04/2016
helpviewer_keywords:
- LIB [C++], extracting library members
- EXTRACT library manager option
- libraries, extracting members
- -EXTRACT library manager option
- extracting library members
- /EXTRACT library manager option
ms.assetid: a2c5c2a1-9b7e-489a-a9a4-1dec694e1fc5
ms.openlocfilehash: 8797db6baa08fc36cf288f5b23d73ff730edd973
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192321"
---
# <a name="extracting-a-library-member"></a>Извлечение члена библиотеки

С помощью программы LIB можно создать файл объекта (obj), содержащий копию члена существующей библиотеки. Чтобы извлечь копию элемента, используйте следующий синтаксис:

```
LIB library /EXTRACT:member /OUT:objectfile
```

Эта команда создает OBJ-файл с именем *обжектфиле* , содержащий копию объекта `member` *библиотеки*. `member`Имя чувствительно к регистру. В одной команде можно извлечь только один элемент. Параметр/OUT является обязательным; имя выхода по умолчанию отсутствует. Если файл с именем *обжектфиле* уже существует в указанном каталоге (или в текущем каталоге, если каталог не указан с помощью *обжектфиле*), то извлеченный *обжектфиле* заменит существующий файл.

## <a name="see-also"></a>См. также раздел

[Справочник по LIB](lib-reference.md)
