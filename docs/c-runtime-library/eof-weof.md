---
description: 'Дополнительные сведения о: EOF, WEOF'
title: EOF, WEOF
ms.date: 11/04/2016
helpviewer_keywords:
- EOF function
- WEOF function
- end of file
ms.assetid: a7150563-cdae-4cdf-9798-ad509990e505
ms.openlocfilehash: 309cf4a8b4c549ae747ef098b99cc050250e0224
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97305030"
---
# <a name="eof-weof"></a>EOF, WEOF

## <a name="syntax"></a>Синтаксис

```
#include <stdio.h>
```

## <a name="remarks"></a>Remarks

Символ EOF возвращается подпрограммой ввода-вывода, если достигнут конец файла (или, в некоторых случаях, если возникла ошибка).

Символ WEOF формирует возвращаемое значение типа **wint_t**, которое используется для сообщения о конце потока расширенных символов или об ошибке.

## <a name="see-also"></a>См. также раздел

[putc, putwc](../c-runtime-library/reference/putc-putwc.md)<br/>
[ungetc, ungetwc](../c-runtime-library/reference/ungetc-ungetwc.md)<br/>
[scanf, _scanf_l, wscanf, _wscanf_l](../c-runtime-library/reference/scanf-scanf-l-wscanf-wscanf-l.md)<br/>
[fflush](../c-runtime-library/reference/fflush.md)<br/>
[fclose, _fcloseall](../c-runtime-library/reference/fclose-fcloseall.md)<br/>
[_ungetch, _ungetwch, _ungetch_nolock, _ungetwch_nolock](../c-runtime-library/reference/ungetch-ungetwch-ungetch-nolock-ungetwch-nolock.md)<br/>
[_putch, _putwch](../c-runtime-library/reference/putch-putwch.md)<br/>
[isascii, __isascii, iswascii](../c-runtime-library/reference/isascii-isascii-iswascii.md)<br/>
[Глобальные константы](../c-runtime-library/global-constants.md)
