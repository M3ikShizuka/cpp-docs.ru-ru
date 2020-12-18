---
description: 'Подробнее о следующем: Ошибки позиции файла'
title: Ошибки позиции файла
ms.date: 11/04/2016
helpviewer_keywords:
- file pointers [C++], file position errors
ms.assetid: d5e59d8b-08c0-4927-a338-0b2d8234ce24
ms.openlocfilehash: d29f8d86280427db915c016fea0fd80567913baf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97196156"
---
# <a name="file-position-errors"></a>Ошибки позиции файла

**ANSI 4.9.9.1, 4.9.9.4** Значение, задаваемое макросу `errno` функциями `fgetpos` и `ftell` при ошибке

В случае сбоя функции `fgetpos` или `ftell` для макроса `errno` задается значение константы `EINVAL` из манифеста, если недопустима позиция, или значение `EBADF`, если недопустим номер файла. Эти константы определены в файле ERRNO.H.

## <a name="see-also"></a>См. также

[Функции библиотеки](../c-language/library-functions.md)
