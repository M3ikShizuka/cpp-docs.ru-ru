---
description: 'Дополнительные сведения о: советы по программированию многобайтовых кодировок'
title: Советы по программированию многобайтовой кодировки
ms.date: 11/04/2016
helpviewer_keywords:
- programming [C++], MBCS
- character sets [C++], multibyte
- MBCS [C++], programming
- multibyte characters [C++]
ms.assetid: d8ad36b8-917f-474e-8adb-69462adecd17
ms.openlocfilehash: 76890f3ecbee6938433bcd2d3fa99023d69e039c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97207193"
---
# <a name="mbcs-programming-tips"></a>Советы по программированию многобайтовой кодировки

В новой разработке следует использовать кодировку символов Юникода для всех строк, которые могут быть доступны конечным пользователям. MBCS — это устаревшая технология, которая заменена Юникодом. В этом разделе приводятся советы для разработчиков, которые должны поддерживать существующие программы, использующие MBCS и непрактичные для преобразования в Юникод. Советы применимы к приложениям и приложениям MFC, написанным без MFC. Будут рассмотрены следующие задачи:

- [Общие рекомендации по программированию многобайтовых кодировок](../text/general-mbcs-programming-advice.md)

- [Увеличение и уменьшение указателей](../text/incrementing-and-decrementing-pointers.md)

- [Индексы байтов](../text/byte-indices.md)

- [Последний символ в строке](../text/last-character-in-a-string.md)

- [Назначение символов](../text/character-assignment.md)

- [Сравнение символов](../text/character-comparison.md)

- [Переполнение буфера](../text/buffer-overflow.md)

## <a name="see-also"></a>См. также раздел

[Поддержка многобайтовых кодировок (MBCS)](../text/support-for-multibyte-character-sets-mbcss.md)
