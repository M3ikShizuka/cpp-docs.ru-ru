---
description: Дополнительные сведения о тексте и строках в Visual C++
title: Текст и строки в Visual C++
ms.date: 11/04/2016
helpviewer_keywords:
- globalization [C++], character sets
- programming [C++], international
- multiple language support [C++]
- Unicode [C++]
- international applications [C++], about international applications
- portability [C++]
- translation [C++], character sets
- non-European characters [C++]
- character sets [C++]
- globalization [C++]
- Japanese characters [C++]
- Kanji character support [C++]
- local character sets [C++]
- ASCII characters [C++]
- character sets [C++], about character sets
- localization [C++], character sets
- translating code [C++]
- localization [C++]
- character sets [C++], non-European
- portability [C++], character sets
- MBCS [C++], international programming
ms.assetid: a1bb27ac-abe5-4c6b-867d-f761d4b93205
ms.openlocfilehash: 3b77df006e095871d11fb3bfbc3d83b081d6052f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335727"
---
# <a name="text-and-strings-in-visual-c"></a>Текст и строки в Visual C++

Важным аспектом разработки приложений для международных рынков является адекватное представление локальных наборов символов. Кодировка ASCII определяет символы в диапазоне от 0x00 до 0x7F. Существуют другие наборы символов, в основном европейские, которые определяют символы в диапазоне от 0x00 до 0x7F, идентичные кодировке ASCII, а также определяют расширенный набор символов от 0x80 до 0xFF. Таким образом, 8-разрядная однобайтовая кодировка (SBCS) достаточно для представления набора символов ASCII, а также наборов символов для многих европейских языков. Однако некоторые неевропейские кодировки, такие как японский символ кандзи, содержат гораздо больше символов, чем может представлять однобайтовую схему кодирования, и поэтому требует кодирования многобайтовой кодировки (MBCS).

## <a name="in-this-section"></a>в этом разделе

[Юникод и многобайтовая кодировка](../text/unicode-and-mbcs.md)<br/>
Описание Visual C++ поддержки Юникода и многобайтовой кодировки.

[Поддержка Юникода](../text/support-for-unicode.md)<br/>
Описывает Юникод, спецификацию для поддержки всех наборов символов, включая наборы символов, которые не могут быть представлены в одном байте.

[Поддержка многобайтовых кодировок (MBCS)](../text/support-for-multibyte-character-sets-mbcss.md)<br/>
Обсуждается многобайтовая кодировка, альтернатива Юникоду для поддержки наборов символов, таких как японский и китайский, которые не могут быть представлены в одном байте.

[Универсальные текстовые сопоставления в файле Tchar. h](../text/generic-text-mappings-in-tchar-h.md)<br/>
Предоставляет универсальные текстовые сопоставления, связанные с Майкрософт, для многих типов данных, подпрограмм и других объектов.

[Практические руководства. преобразование между различными строковыми типами](../text/how-to-convert-between-various-string-types.md)<br/>
Демонстрирует преобразование различных Visual C++ строковых типов в другие строки.

## <a name="related-sections"></a>Связанные разделы

[Интернационализация](../c-runtime-library/internationalization.md)<br/>
Обсуждается международная поддержка в библиотеке времени выполнения C.

[Международные примеры](https://github.com/Microsoft/VCSamples/tree/master/VC2010Samples/International)<br/>
Ссылки на примеры, демонстрирующие многоязыковую поддержку в Visual C++.

[Locale Names, Languages, and Country/Region Strings](../c-runtime-library/locale-names-languages-and-country-region-strings.md) (Строки страны или региона и языка)<br/>
Предоставляет строки языка и страны или региона в библиотеке времени выполнения C.
