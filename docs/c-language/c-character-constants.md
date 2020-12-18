---
description: 'Подробнее о следующем: Константы символов в C'
title: Константы символов в C
ms.date: 11/04/2016
helpviewer_keywords:
- characters, constants
- (') single quotation mark
- constants, character
- single quotation mark
ms.assetid: 388ae7d7-2c3a-44d6-a507-63f541ecd2da
ms.openlocfilehash: 2503fc983d79f363f525b22172d2113393b41091
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97211561"
---
# <a name="c-character-constants"></a>Константы символов в C

"Константа символа" создается путем заключения одного символа из набора представимых символов в одинарные кавычки ( **' '** ). Константы символов используются для представления символов в [кодировке выполнения](../c-language/execution-character-set.md).

## <a name="syntax"></a>Синтаксис

*character-constant*: **'** *c-char-sequence* **'**

**L'** *c-char-sequence* **'**

*c-char-sequence*: *c-char*

*c-char-sequence c-char*

*c-char*: Любой член исходной кодировки, кроме одинарной кавычки ( **'** ), обратной косой черты ( **\\** ) и символа новой строки

*escape-sequence*

*escape-sequence*: *simple-escape-sequence*

*octal-escape-sequence*

*hexadecimal-escape-sequence*

*simple-escape-sequence*: один из символов: **\a \b \f \n \r \t \v**

**\\' \\" \\\ \\?**

*octal-escape-sequence*: **\\**  *octal-digit*

**\\**  *octal-digit octal-digit*

**\\**  *octal-digit octal-digit octal-digit*

*hexadecimal-escape-sequence*: **\x**  *hexadecimal-digit*

*hexadecimal-escape-sequence hexadecimal-digit*

## <a name="see-also"></a>См. также

[Константы в C](../c-language/c-constants.md)
