---
title: Language Strings
description: Дополнительные сведения о строках языка
ms.date: 1/12/2021
helpviewer_keywords:
- language strings
ms.openlocfilehash: ec82bb8b9efb9c366c287c79b71b60a3c6bc6ab2
ms.sourcegitcommit: b51f79b5394e12cd90cb65c85cc01716f90bfc90
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/13/2021
ms.locfileid: "98167025"
---
# <a name="language-strings"></a>Language Strings

[`setlocale`](../c-runtime-library/reference/setlocale-wsetlocale.md)Функции и [`_create_locale`](../c-runtime-library/reference/create-locale-wcreate-locale.md) могут использовать ПОДДЕРЖИВАЕМЫЕ языки API NLS Windows в операционных системах, которые не используют кодовую страницу Юникода. Список поддерживаемых языков по версии операционной системы см. [в приложении a: поведение продукта](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c) в \[ MS-LCID]: Справочник по идентификатору языка (LCID) Windows. Строка языка может принимать любое из значений, перечисленных в столбцах **Язык** и **Тег языка** списка поддерживаемых языков. Пример кода, который перечисляет доступные имена языковых стандартов и связанные значения, см. в разделе [NLS: пример интерфейсов API на основе имен](/windows/win32/intl/nls--name-based-apis-sample).

## <a name="supported-language-strings"></a>Поддерживаемые строки языка

Реализация библиотеки времени выполнения C от Майкрософт также поддерживает эти строки языка:

|Строка языка|Соответствующее название языкового стандарта|
|---------------------|----------------------------|
|`american`|`en-US`|
|`american english`|`en-US`|
|`american-english`|`en-US`|
|`australian`|`en-AU`|
|`belgian`|`nl-BE`|
|`canadian`|`en-CA`|
|`chh`|`zh-HK`|
|`chi`|`zh-SG`|
|`chinese`|`zh`|
|`chinese-hongkong`|`zh-HK`|
|`chinese-simplified`|`zh-CN`|
|`chinese-singapore`|`zh-SG`|
|`chinese-traditional`|`zh-TW`|
|`dutch-belgian`|`nl-BE`|
|`english-american`|`en-US`|
|`english-aus`|`en-AU`|
|`english-belize`|`en-BZ`|
|`english-can`|`en-CA`|
|`english-caribbean`|`en-029`|
|`english-ire`|`en-IE`|
|`english-jamaica`|`en-JM`|
|`english-nz`|`en-NZ`|
|`english-south africa`|`en-ZA`|
|`english-trinidad y tobago`|`en-TT`|
|`english-uk`|`en-GB`|
|`english-us`|`en-US`|
|`english-usa`|`en-US`|
|`french-belgian`|`fr-BE`|
|`french-canadian`|`fr-CA`|
|`french-luxembourg`|`fr-LU`|
|`french-swiss`|`fr-CH`|
|`german-austrian`|`de-AT`|
|`german-lichtenstein`|`de-LI`|
|`german-luxembourg`|`de-LU`|
|`german-swiss`|`de-CH`|
|`irish-english`|`en-IE`|
|`italian-swiss`|`it-CH`|
|`norwegian`|`no`|
|`norwegian-bokmal`|`nb-NO`|
|`norwegian-nynorsk`|`nn-NO`|
|`portuguese-brazilian`|`pt-BR`|
|`spanish-argentina`|`es-AR`|
|`spanish-bolivia`|`es-BO`|
|`spanish-chile`|`es-CL`|
|`spanish-colombia`|`es-CO`|
|`spanish-costa rica`|`es-CR`|
|`spanish-dominican republic`|`es-DO`|
|`spanish-ecuador`|`es-EC`|
|`spanish-el salvador`|`es-SV`|
|`spanish-guatemala`|`es-GT`|
|`spanish-honduras`|`es-HN`|
|`spanish-mexican`|`es-MX`|
|`spanish-modern`|`es-ES`|
|`spanish-nicaragua`|`es-NI`|
|`spanish-panama`|`es-PA`|
|`spanish-paraguay`|`es-PY`|
|`spanish-peru`|`es-PE`|
|`spanish-puerto rico`|`es-PR`|
|`spanish-uruguay`|`es-UY`|
|`spanish-venezuela`|`es-VE`|
|`swedish-finland`|`sv-FI`|
|`swiss`|`de-CH`|
|`uk`|`en-GB`|
|`us`|`en-US`|
|`usa`|`en-US`|

## <a name="see-also"></a>См. также

- [Имена языковых стандартов, языки и строки страны или региона](../c-runtime-library/locale-names-languages-and-country-region-strings.md)\
- [Строки страны или региона](../c-runtime-library/country-region-strings.md)\
- [`setlocale`, `_wsetlocale`](../c-runtime-library/reference/setlocale-wsetlocale.md)\
- [`_create_locale`, `_wcreate_locale`](../c-runtime-library/reference/create-locale-wcreate-locale.md)
