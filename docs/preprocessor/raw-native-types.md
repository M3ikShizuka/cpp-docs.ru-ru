---
description: 'Дополнительные сведения: raw_native_types атрибута импорта'
title: raw_native_types атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- raw_native_types
helpviewer_keywords:
- raw_native_types attribute
ms.assetid: 9f38daa8-8dc0-46a5-aff9-f1ff9c1e6f48
ms.openlocfilehash: 64eaadcbb3d9f07d47dd4a33bc16a222cae50f38
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97240537"
---
# <a name="raw_native_types-import-attribute"></a>raw_native_types атрибут импорта

**Блок, относящийся только к языку C++**

Отключает использование классов поддержки COM в функциях-оболочках высокого уровня и принудительное использование типов данных низкого уровня.

## <a name="syntax"></a>Синтаксис

> **raw_native_types** типов **#import** *-Library*

## <a name="remarks"></a>Комментарии

По умолчанию методы обработки ошибок высокого уровня используют классы поддержки COM [_bstr_t](../cpp/bstr-t-class.md) и [_variant_t](../cpp/variant-t-class.md) вместо `BSTR` `VARIANT` типов данных и и необработанных указателей COM-интерфейсов. Эти классы инкапсулируют сведения выделения и отмены выделения хранилища памяти для этих типов данных и значительно упрощают операции приведения и преобразования типов.

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
