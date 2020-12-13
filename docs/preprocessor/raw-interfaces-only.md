---
description: 'Дополнительные сведения: raw_interfaces_only атрибута импорта'
title: raw_interfaces_only атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- raw_interfaces_only
helpviewer_keywords:
- raw_interfaces_only attribute
ms.assetid: 87056c6d-3f34-4248-af58-f5775a35bfb7
ms.openlocfilehash: f043bef5cde0454ce9f08f45efb0417aa7fdbb2d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142744"
---
# <a name="raw_interfaces_only-import-attribute"></a>raw_interfaces_only атрибут импорта

**Блок, относящийся только к языку C++**

Подавляет создание функций-оболочек обработки ошибок и объявлений [свойств](../cpp/property-cpp.md) , использующих эти функции-оболочки.

## <a name="syntax"></a>Синтаксис

> **raw_interfaces_only** типов **#import** *-Library*

## <a name="remarks"></a>Комментарии

Атрибут **raw_interfaces_only** также вызывает префикс по умолчанию, используемый при именовании удаляемых функций, не являющихся свойствами. Как правило, префикс имеет значение `raw_` . Если этот атрибут указан, имена функций берутся непосредственно из библиотеки типов.

Этот атрибут позволяет предоставлять только низкоуровневое содержимое библиотеки типов.

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
