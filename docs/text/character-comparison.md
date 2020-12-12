---
description: 'Дополнительные сведения: сравнение символов'
title: Сравнение знаков
ms.date: 11/04/2016
helpviewer_keywords:
- comparing characters
- MBCS [C++], character comparison
- characters [C++], comparing
ms.assetid: 18846e44-3e6e-40c4-9b42-3153fb15db20
ms.openlocfilehash: 0e00e087074a70145f1a73694293edc3c522d69f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297009"
---
# <a name="character-comparison"></a>Сравнение знаков

Используйте следующие советы.

- Сравнение известного старший байт с символом ASCII работает правильно:

    ```cpp
    if( *sz1 == 'A' )
    ```

- Сравнение двух неизвестных символов требует использования одного из макросов, определенных в mbstring. h:

    ```cpp
    if( !_mbccmp( sz1, sz2) )
    ```

   Это гарантирует, что оба байта двухбайтовых символов будут сравниваться на равенство.

## <a name="see-also"></a>См. также раздел

[Советы по программированию многобайтовых кодировок](../text/mbcs-programming-tips.md)<br/>
[Переполнение буфера](../text/buffer-overflow.md)
