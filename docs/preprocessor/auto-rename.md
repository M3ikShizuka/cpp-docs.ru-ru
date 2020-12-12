---
description: 'Дополнительные сведения: auto_rename атрибута импорта'
title: auto_rename атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- auto_rename
helpviewer_keywords:
- auto_rename attribute
ms.assetid: 1075f3ab-f6fc-4e04-8e22-ebe02695a567
ms.openlocfilehash: 57406b1f64b3e5e484556ae15600cc30f1e931dd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97301039"
---
# <a name="auto_rename-import-attribute"></a>auto_rename атрибут импорта

**Блок, относящийся только к языку C++**

Переименовывает зарезервированные слова C++ путем добавления двух знаков подчеркивания (__) к именам переменных, чтобы разрешить потенциальные конфликты имен.

## <a name="syntax"></a>Синтаксис

> **auto_rename** типов **#import** *-Library*

## <a name="remarks"></a>Комментарии

Этот атрибут используется при импорте библиотеки типов, в которой в качестве имен переменных используется одно или несколько зарезервированных слов C или C++ (ключевых слов или макросов).

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
