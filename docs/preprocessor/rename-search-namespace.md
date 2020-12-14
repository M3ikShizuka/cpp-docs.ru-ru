---
description: 'Дополнительные сведения: rename_search_namespace атрибута импорта'
title: rename_search_namespace атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- rename_search_namespace
helpviewer_keywords:
- rename_search_namespace attribute
ms.assetid: 47c9d7fd-59dc-4c62-87a1-9011a0040167
ms.openlocfilehash: 36bbb96c23e729bb5294a75f52b65b3ec60219cb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97342313"
---
# <a name="rename_search_namespace-import-attribute"></a>rename_search_namespace атрибут импорта

**Блок, относящийся только к языку C++**

Функция имеет те же функциональные возможности, что и атрибут [rename_namespace](../preprocessor/rename-namespace.md) , но используется в библиотеках типов, где используется `#import` директива вместе с атрибутом [auto_search](../preprocessor/auto-search.md) .

## <a name="syntax"></a>Синтаксис

> rename_search_namespace типов **#import** *-Library* **(** "*новое_имя*" **)**

### <a name="parameters"></a>Параметры

*NewName*\
Новое имя пространства имен.

## <a name="remarks"></a>Комментарии

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
