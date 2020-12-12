---
description: 'Дополнительные сведения: high_property_prefixes атрибута импорта'
title: high_property_prefixes атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- high_property_prefixes
helpviewer_keywords:
- high_property_prefixes attribute
ms.assetid: 91c6cc2b-19b6-4aba-8831-d9e5cccb58b5
ms.openlocfilehash: af6835f5835c23dceadbb5152e36b0dabcbb8c98
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167478"
---
# <a name="high_property_prefixes-import-attribute"></a>high_property_prefixes атрибут импорта

**Блок, относящийся только к языку C++**

Задает другие префиксы для трех методов свойств.

## <a name="syntax"></a>Синтаксис

> **#import** *Type-Library* **high_property_prefixes (** "*префикс*" **,** "*путпрефикс*" **,** "*путрефпрефикс*" **)**

### <a name="parameters"></a>Параметры

*Префикс*\
Префикс, который будет использоваться для `propget` методов.

*путпрефикс*\
Префикс, который будет использоваться для `propput` методов.

*путрефпрефикс*\
Префикс, который будет использоваться для `propputref` методов.

## <a name="remarks"></a>Комментарии

По умолчанию высокоуровневые методы обработки ошибок `propget` , `propput` и `propputref` предоставляются функциями-членами с префиксами `Get` , `Put` и `PutRef` соответственно.

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
