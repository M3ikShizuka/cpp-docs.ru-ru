---
description: 'Подробнее о следующем: Тестирование символов'
title: Тестирование символов
ms.date: 11/04/2016
ms.assetid: 376ba061-bae3-427e-9569-33fa5949a199
ms.openlocfilehash: b7d73bce671787622814e11d8f3add7a1092572a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190540"
---
# <a name="character-testing"></a>Тестирование символов

**ANSI 4.3.1** Наборы символов, тестируемые функциями `isalnum`, `isalpha`, `iscntrl`, `islower`, `isprint` и `isupper`

В следующей таблице приведено описание этих функций в соответствии с реализацией компилятором Microsoft C.

|Функция|Тестируемые наборы символов|
|--------------|---------------|
|`isalnum`|Символы 0–9, A–Z, a–z (коды ASCII 48–57, 65–90, 97–122)|
|`isalpha`|Символы A–Z, a–z (коды ASCII 65–90, 97–122)|
|`iscntrl`|Коды ASCII 0–31, 127|
|`islower`|Символы a–z (коды ASCII 97–122)|
|`isprint`|Символы A–Z, a–z, 0–9, пунктуация, пробел (коды ASCII 32–126)|
|`isupper`|Символы A–Z (коды ASCII 65–90)|

## <a name="see-also"></a>См. также

[Функции библиотеки](../c-language/library-functions.md)
