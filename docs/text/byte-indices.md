---
description: 'Дополнительные сведения: байтовые индексы'
title: Индексы байтов
ms.date: 11/04/2016
helpviewer_keywords:
- MBCS [C++], byte indices
- byte indices [C++]
ms.assetid: f6e7774a-86c6-41c2-89e3-74fd46432e47
ms.openlocfilehash: 5ee4b2cb8611893c71f5c6597e619cc73e2848ef
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97187563"
---
# <a name="byte-indices"></a>Индексы байтов

Используйте следующие советы.

- Работа с индексом битевисе в строке представляет проблемы, аналогичные тем, которые возникают при манипуляции указателями. Рассмотрим этот пример, который проверяет строку на наличие символа обратной косой черты:

    ```cpp
    while ( rgch[ i ] != '\\' )
        i++;
    ```

   Это может индексировать конечный байт, а не старший байт, поэтому он может не указывать на `character` .

- Чтобы решить предыдущую проблему, используйте функцию [_mbclen](../c-runtime-library/reference/mbclen-mblen-mblen-l.md) .

    ```cpp
    while ( rgch[ i ] != '\\' )
        i += _mbclen ( rgch + i );
    ```

   Это верно индексирует старший байт и, следовательно, на `character` . `_mbclen`Функция определяет размер символа (1 или 2 байта).

## <a name="see-also"></a>См. также раздел

[Советы по программированию многобайтовых кодировок](../text/mbcs-programming-tips.md)<br/>
[Последний символ в строке](../text/last-character-in-a-string.md)
