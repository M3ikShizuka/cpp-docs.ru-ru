---
title: Строки стран и регионов
description: Дополнительные сведения о строках страны и региона
ms.date: 1/29/2020
helpviewer_keywords:
- country/region strings
ms.openlocfilehash: 34494eb2bcace615e72127ab1735101809e8ade5
ms.sourcegitcommit: beac3ddf1a20de5e836569ae07407d5f3703f536
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2021
ms.locfileid: "99224441"
---
# <a name="countryregion-strings"></a>строки страны и региона

Строки страны и региона можно объединять со строкой с названием языка для создания спецификации языкового стандарта для функций `setlocale`, `_wsetlocale`, `_create_locale`и `_wcreate_locale` . 

Список названий стран и регионов, поддерживаемых различными версиями операционных систем Windows, см. в разделе столбцы **языка**, **расположения** и **языка** таблицы в [приложении а. поведение продукта](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c) в \[ MS-LCID]: Справочник по идентификатору языка (LCID) Windows. Пример кода для перечисления имен доступных языковых стандартов и связанных значений см. в руководстве по [многоязыковой поддержке с примером API на основе имени](/windows/win32/intl/nls--name-based-apis-sample).

## <a name="additional-supported-country-and-region-strings"></a>Дополнительные поддерживаемые строки страны и региона

Реализация библиотеки времени выполнения C от Майкрософт также поддерживает следующие дополнительные строки и аббревиатуры стран и регионов:

|Строка страны или региона|Сокращение|Соответствующее название языкового стандарта|
|----------------------------|------------------|----------------------------|
|`america`|`USA`|`en-US`|
|`britain`|`GBR`|`en-GB`|
|`china`|`CHN`|`zh-CN`|
|`czech`|`CZE`|`cs-CZ`|
|`england`|`GBR`|`en-GB`|
|`great britain`|`GBR`|`en-GB`|
|`holland`|`NLD`|`nl-NL`|
|`hong-kong`|`HKG`|`zh-HK`|
|`new-zealand`|`NZL`|`en-NZ`|
|`nz`|`NZL`|`en-NZ`|
|`pr china`|`CHN`|`zh-CN`|
|`pr-china`|`CHN`|`zh-CN`|
|`puerto-rico`|`PRI`|`es-PR`|
|`slovak`|`SVK`|`sk-SK`|
|`south africa`|`ZAF`|`af-ZA`|
|`south korea`|`KOR`|`ko-KR`|
|`south-africa`|`ZAF`|`af-ZA`|
|`south-korea`|`KOR`|`ko-KR`|
|`trinidad & tobago`|`TTO`|`en-TT`|
|`uk`|`GBR`|`en-GB`|
|`united-kingdom`|`GBR`|`en-GB`|
|`united-states`|`USA`|`en-US`|
|`us`|`USA`|`en-US`|

## <a name="see-also"></a>См. также

[Имена языковых стандартов, языки и строки страны или региона](../c-runtime-library/locale-names-languages-and-country-region-strings.md)<br/>
[Строки языка](../c-runtime-library/language-strings.md)<br/>
[setlocale, _wsetlocale](../c-runtime-library/reference/setlocale-wsetlocale.md)<br/>
[_create_locale, _wcreate_locale](../c-runtime-library/reference/create-locale-wcreate-locale.md)
