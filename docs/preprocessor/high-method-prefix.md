---
description: 'Дополнительные сведения: high_method_prefix атрибута импорта'
title: high_method_prefix атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- high_method_prefix
helpviewer_keywords:
- high_method_prefix attribute
ms.assetid: cacebf09-12f5-4919-ad40-939e206e340c
ms.openlocfilehash: 0ebf73892ad1ea544f3deee726695bb8e209cb2c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167491"
---
# <a name="high_method_prefix-import-attribute"></a>high_method_prefix атрибут импорта

**Блок, относящийся только к языку C++**

Задает префикс, используемый при именовании высокоуровневых свойств и методов.

## <a name="syntax"></a>Синтаксис

> **#import** high_method_prefix *типа-Library* **(** "*префикс*" **)**

### <a name="parameters"></a>Параметры

*Prefix*\
Префикс, который следует использовать.

## <a name="remarks"></a>Комментарии

По умолчанию высокоуровневые свойства и методы обработки ошибок предоставляются функциями-членами с именами без префикса. Это имена из библиотеки типов.

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
