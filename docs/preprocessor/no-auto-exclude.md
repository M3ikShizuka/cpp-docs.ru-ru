---
description: 'Дополнительные сведения: no_auto_exclude атрибута импорта'
title: no_auto_exclude атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- no_auto_exclude
helpviewer_keywords:
- no_auto_exclude attribute
ms.assetid: 3241ef9c-758a-4e86-bdc5-37da6072430f
ms.openlocfilehash: 81e4d7e7f9295a4ed983e2a5024d891e30fe1361
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333351"
---
# <a name="no_auto_exclude-import-attribute"></a>no_auto_exclude атрибут импорта

**Блок, относящийся только к языку C++**

Отключает автоматическое исключение.

## <a name="syntax"></a>Синтаксис

> **no_auto_exclude** типов **#import** *-Library*

## <a name="remarks"></a>Комментарии

Библиотеки типов могут содержать определения элементов, которые определены в системных заголовочных файлах или других библиотеках типов. Директива `#import` пытается предотвратить ошибки об использовании нескольких определений, автоматически исключая такие элементы. Это приводит к тому, что для каждого исключаемого элемента выдается [Предупреждение компилятора (уровень 3) C4192](../error-messages/compiler-warnings/compiler-warning-level-3-c4192.md) . Вы можете отключить автоматическое исключение с помощью этого атрибута.

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
