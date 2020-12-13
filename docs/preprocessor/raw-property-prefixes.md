---
description: 'Дополнительные сведения: raw_property_prefixes атрибута импорта'
title: raw_property_prefixes атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- raw_property_prefixes
helpviewer_keywords:
- raw_property_prefixes attribute
ms.assetid: 03a0f48c-c460-4175-a762-9f7f8d84b12f
ms.openlocfilehash: 7289f9aeba249249ecf78ffb3ad3b32669ac9fe3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142718"
---
# <a name="raw_property_prefixes-import-attribute"></a>raw_property_prefixes атрибут импорта

**Блок, относящийся только к языку C++**

Задает другие префиксы для трех методов свойств.

## <a name="syntax"></a>Синтаксис

> **#import** *Type-Library* **raw_property_prefixes (** "*префикс*" **,** "*путпрефикс*" **,** "*путрефпрефикс*" **)**

### <a name="parameters"></a>Параметры

*Префикс*\
Префикс, используемый для `propget` методов.

*путпрефикс*\
Префикс, используемый для `propput` методов.

*путрефпрефикс*\
Префикс, используемый для `propputref` методов.

## <a name="remarks"></a>Комментарии

По умолчанию методы низкого уровня `propget` , `propput` и `propputref` предоставляются функциями-членами с именем с помощью префиксов `get_` , `put_` и `putref_` соответственно. Эти префиксы совместимы с именами, используемыми в файлах заголовков, которые генерирует MIDL.

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
