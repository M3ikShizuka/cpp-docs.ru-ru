---
description: Дополнительные сведения о сопоставлениях типов данных
title: Сопоставления типов данных
ms.date: 11/04/2016
f1_keywords:
- _TXCHAR
- _TUCHAR
- _TINT
- _TSCHAR
- _TCHAR
- TCHAR::H
- TCHAR
- _T
- _TEXT
helpviewer_keywords:
- _TXCHAR type
- TINT type
- _TCHAR type
- TSCHAR type
- TEXT type
- TCHAR type
- TCHAR.H data types, mappings defined in
- generic-text data types
- _TINT type
- TUCHAR type
- TXCHAR type
- _TSCHAR type
- T type
- _TUCHAR type
- _TEXT type
- _T type
ms.assetid: 4e573c05-8800-468b-ae5f-76ff7409835e
ms.openlocfilehash: 9d76ecebc9bcb01e86cac2f199534ae2cda518c8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97258784"
---
# <a name="data-type-mappings"></a>Сопоставления типов данных

Сопоставления типов данных определяются в TCHAR.H и зависят от того, определена ли в вашей программе константа `_UNICODE` или `_MBCS`.

Дополнительные сведения см. в разделе [Использование типов данных TCHAR.H с кодом _MBCS](../text/using-tchar-h-data-types-with-mbcs-code.md).

### <a name="generic-text-data-type-mappings"></a>Сопоставления типов данных универсального текста

|Универсальный текст<br /><br /> имя типа данных|SBCS (_UNICODE,<br /><br /> _MBCS не<br /><br /> определен)|_MBCS<br /><br /> defined|_UNICODE<br /><br /> defined|
|--------------------------------------|----------------------------------------------------|------------------------|---------------------------|
|`_TCHAR`|**`char`**|**`char`**|**`wchar_t`**|
|`_tfinddata_t`|`_finddata_t`|`_finddata_t`|`_wfinddata_t`|
|`_tfinddata64_t`|`__finddata64_t`|`__finddata64_t`|`__wfinddata64_t`|
|`_tfinddatai64_t`|`_finddatai64_t`|`_finddatai64_t`|`_wfinddatai64_t`|
|`_TINT`|**`int`**|**`int`**|`wint_t`|
|`_TSCHAR`|**`signed char`**|**`signed char`**|**`wchar_t`**|
|`_TUCHAR`|**`unsigned char`**|**`unsigned char`**|**`wchar_t`**|
|`_TXCHAR`|**`char`**|**`unsigned char`**|**`wchar_t`**|
|`_T` или `_TEXT`|Не действует (удаляется препроцессором)|Не действует (удаляется препроцессором)|`L` (преобразует следующий символ или строку в аналог в Юникоде)|

## <a name="see-also"></a>См. также раздел

[Универсальные текстовые сопоставления](../c-runtime-library/generic-text-mappings.md)<br/>
[Сопоставления констант и глобальных переменных](../c-runtime-library/constant-and-global-variable-mappings.md)<br/>
[Сопоставления подпрограмм](../c-runtime-library/routine-mappings.md)<br/>
[Пример программы Generic-Text](../c-runtime-library/a-sample-generic-text-program.md)<br/>
[Использование сопоставлений Generic-Text](../c-runtime-library/using-generic-text-mappings.md)
