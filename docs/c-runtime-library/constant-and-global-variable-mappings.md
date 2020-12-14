---
description: Дополнительные сведения см. в статье сопоставления констант и глобальных переменных.
title: Сопоставления констант и глобальных переменных
ms.date: 11/04/2016
f1_keywords:
- _tenviron
- _TEOF
- _tfinddata_t
helpviewer_keywords:
- tfinddatat function
- tenviron function
- TEOF type
- _TEOF type
- generic-text mappings
- _tenviron function
- _tfinddata_t function
ms.assetid: 3af4fd3e-9ed5-4ed9-96fd-7031e5126fd1
ms.openlocfilehash: 6078564a5f9d6ef28de704f4991264b5de58041b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97195766"
---
# <a name="constant-and-global-variable-mappings"></a>Сопоставления констант и глобальных переменных

Сопоставления универсальных текстовых констант, глобальных переменных и стандартных типов определяются в TCHAR.H и зависят от того, определена ли в вашей программе константа `_UNICODE` или `_MBCS`.

### <a name="generic-text-constant-and-global-variable-mappings"></a>Сопоставления универсальных текстовых констант и глобальных переменных

|Универсальный текст - имя объекта|Однобайтовая кодировка (_UNICODE, _MBCS не определены)|_MBCS определено|_UNICODE определено|
|----------------------------------|--------------------------------------------|--------------------|-----------------------|
|`_TEOF`|`EOF`|`EOF`|`WEOF`|
|`_tenviron`|`_environ`|`_environ`|`_wenviron`|
|`_tpgmptr`|`_pgmptr`|`_pgmptr`|`_wpgmptr`|

## <a name="see-also"></a>См. также раздел

[Универсальные текстовые сопоставления](../c-runtime-library/generic-text-mappings.md)<br/>
[Сопоставления типов данных](../c-runtime-library/data-type-mappings.md)<br/>
[Сопоставления подпрограмм](../c-runtime-library/routine-mappings.md)<br/>
[Пример программы Generic-Text](../c-runtime-library/a-sample-generic-text-program.md)<br/>
[Использование сопоставлений Generic-Text](../c-runtime-library/using-generic-text-mappings.md)
