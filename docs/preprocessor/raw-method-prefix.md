---
description: 'Дополнительные сведения: raw_method_prefix'
title: raw_method_prefix
ms.date: 08/29/2019
f1_keywords:
- raw_method_prefix
helpviewer_keywords:
- raw_method_prefix attribute
ms.assetid: 71490313-af78-4bb2-b28a-eee67950d30b
ms.openlocfilehash: 9e05f70814e48a4460287e96905b543f7d76dde6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201993"
---
# <a name="raw_method_prefix"></a>raw_method_prefix

**Блок, относящийся только к языку C++**

Указывает другой префикс, чтобы избежать конфликтов имен.

## <a name="syntax"></a>Синтаксис

> **#import** raw_method_prefix *типа-Library* **(** "*префикс*" **)**

### <a name="parameters"></a>Параметры

*Prefix*\
Необходимый префикс.

## <a name="remarks"></a>Комментарии

Низкоуровневые свойства и методы предоставляются функциями-членами с именами, использующими префикс по умолчанию **raw_**, чтобы избежать конфликтов имен с функциями-членами, обрабатывающими ошибки высокого уровня.

> [!NOTE]
> Влияние атрибута **raw_method_prefix** не изменилось на наличие атрибута [raw_interfaces_only](raw-interfaces-only.md) . **Raw_method_prefix** всегда имеет приоритет над `raw_interfaces_only` указанием префикса. Если в одной инструкции используются оба атрибута `#import` , то используется префикс, заданный атрибутом **raw_method_prefix** .

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
