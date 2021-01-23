---
title: Общие сведения о грамматике препроцессора (C/C++)
description: Определяет и описывает синтаксис препроцессора компилятора Microsoft C/C++ (КОМПИЛЯТОРОМ MSVC).
ms.date: 01/22/2021
helpviewer_keywords:
- grammar
- preprocessor, grammar
ms.openlocfilehash: dbe46a67337bf55cb98100878dedb8c92120472b
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713640"
---
# <a name="preprocessor-grammar-summary-cc"></a>Общие сведения о грамматике препроцессора (C/C++)

В этой статье описывается формальное грамматика препроцессора C и C++. Он охватывает синтаксис директив и операторов предварительной обработки. Дополнительные сведения см. в разделе директивы [препроцессора](../preprocessor/preprocessor.md) и директивы [pragma, а также `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md).

## <a name="definitions-for-the-grammar-summary"></a><a name="definitions"></a> Определения для сводки грамматики

Терминальные слова — это конечные точки в определении синтаксиса. Никакое другое разрешение невозможно. Терминальные слова включают в себя набор зарезервированных ключевых слов и определенные пользователем идентификаторы.

Нетерминальные слова — это местозаполнители в синтаксисе. Большая их часть определена в других местах этой сводки синтаксиса. Определения могут быть рекурсивными. Следующие Нетерминальные значения определены в разделе " [лексические соглашения](../cpp/lexical-conventions.md) " *справочника по языку C++*:

*`constant`*, *`constant-expression`*, *`identifier`*, *`keyword`*, *`operator`*, *`punctuator`*

Необязательный компонент обозначается атрибутом <sub>opt</sub> в нижнем индексе. Например, следующий синтаксис указывает необязательное выражение, заключенное в фигурные скобки:

**`{`***`expression`* <sub>неявное согласие</sub>**`}`**

## <a name="document-conventions"></a><a name="conventions"></a> Соглашения о документе

В соглашениях используются разные атрибуты шрифтов для различных компонентов синтаксиса. Ниже перечислены символы и шрифты.

| Атрибут | Описание |
|---------------|-----------------|
| *`nonterminal`* | Курсивом выделяются нетерминальные символы. |
| **`#include`** | Терминальные символы, выделенные жирным шрифтом, представляют литеральные зарезервированные слова и символы, которые должны вводиться, как показано. В знаках в этом контексте всегда учитывается регистр. |
| <sub>opt</sub> | Нетерминальные символы, за которыми следует атрибут <sub>opt</sub>, всегда являются необязательными.|
| Шрифт по умолчанию | Знаки в наборе, описанные или перечисленные в этом шрифте, можно использовать в качестве терминальных символов в операторах. |

**`:`** После нетерминального двоеточия () вводит его определение. Альтернативные определения перечисляются в отдельных строках.

В блоках синтаксиса кода эти символы в гарнитуре по умолчанию имеют специальное значение:

| Символ | Описание |
|---|---|
| \[ ] | Необязательный элемент заключается в квадратные скобки. |
| { \| } | Фигурные скобки разделяют альтернативные элементы, разделенные вертикальными линиями. |
| ... | Указывает, что предыдущий шаблон элемента можно повторить. |

В блоках синтаксиса кода, запятые ( `,` ), Periods ( `.` ), точки с запятой ( `;` ), двоеточия ( `:` ), круглые скобки ( `( )` ), двойные кавычки () `"` и одинарные кавычки ( `'` ) являются литералами.

## <a name="preprocessor-grammar"></a><a name="grammar"></a> Грамматика препроцессора

*`control-line`*:\
&emsp;**`#define`***`identifier`* *`token-string`* <sub>неявное согласие</sub>\
&emsp;**`#define`***`identifier`* **`(`** *`identifier`* <sub>неявное согласие</sub> **`,`** ... **`,`** *`identifier`* <sub>неявное согласие</sub> **`)`** *`token-string`* <sub>неявное согласие</sub>\
&emsp;**`#include`** **`"`**_`path-spec`_**`"`**\
&emsp;**`#include`** **`<`**_`path-spec`_**`>`**\
&emsp;**`#line`***`digit-sequence`* **`"`**_`filename`_**`"`** <sub>неявное согласие</sub>\
&emsp;**`#undef`** *`identifier`*\
&emsp;**`#error`** *`token-string`*\
&emsp;**`#pragma`** *`token-string`*

*`constant-expression`*:\
&emsp;**`defined(`** *`identifier`* **`)`**\
&emsp;**`defined`** *`identifier`*\
&emsp;любое другое константное выражение

*`conditional`*:\
&emsp; *`if-part`* *`elif-parts`* <sub>необ.</sub> *`else-part`* <sub>необ.</sub> *`endif-line`*

*`if-part`*:\
&emsp;*`if-line`* *`text`*

*`if-line`*:\
&emsp;**`#if`** *`constant-expression`*\
&emsp;**`#ifdef`** *`identifier`*\
&emsp;**`#ifndef`** *`identifier`*

*`elif-parts`*:\
&emsp;*`elif-line`* *`text`*\
&emsp;*`elif-parts`* *`elif-line`* *`text`*

*`elif-line`*:\
&emsp;**`#elif`** *`constant-expression`*

*`else-part`*:\
&emsp;*`else-line`* *`text`*

*`else-line`*:\
&emsp;**`#else`**

*`endif-line`*:\
&emsp;**`#endif`**

*`digit-sequence`*:\
&emsp;*`digit`*\
&emsp;*`digit-sequence`* *`digit`*

*`digit`* : один из\
&emsp;**`0` `1` `2` `3` `4` `5` `6` `7` `8` `9`**

*`token-string`*:\
&emsp;Строка *`token`*

*`token`*:\
&emsp;*`keyword`*\
&emsp;*`identifier`*\
&emsp;*`constant`*\
&emsp;*`operator`*\
&emsp;*`punctuator`*

*`filename`*:\
&emsp;Допустимое имя файла в ОС

*`path-spec`*:\
&emsp;Допустимый путь к файлу

*`text`*:\
&emsp;Любая текстовая последовательность

> [!NOTE]
> Следующие Нетерминальные значения расширены в разделе [лексические обозначения](../cpp/lexical-conventions.md) *справочника по языку C++*: *`constant`* , *`constant-expression`* , *`identifier`* ,, *`keyword`* *`operator`* и *`punctuator`* .

## <a name="see-also"></a>См. также раздел

[Справочник по препроцессору в C/C++](../preprocessor/c-cpp-preprocessor-reference.md)
