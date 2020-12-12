---
description: 'Дополнительные сведения: rename_namespace атрибута импорта'
title: rename_namespace атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- rename_namespace
helpviewer_keywords:
- rename_namespace attribute
ms.assetid: 45006d2b-36cd-4bec-98b9-3b8ec45299e3
ms.openlocfilehash: 402d9c9cd8dee5979dd71e16fec1a606d8b4b996
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167387"
---
# <a name="rename_namespace-import-attribute"></a>rename_namespace атрибут импорта

**Блок, относящийся только к языку C++**

Переименовывает пространство имен, к которому относится содержимое библиотеки типов.

## <a name="syntax"></a>Синтаксис

> rename_namespace типов **#import** *-Library* **(** "*новое_имя*" **)**

### <a name="parameters"></a>Параметры

*NewName*\
Новое имя пространства имен.

## <a name="remarks"></a>Комментарии

Атрибут **rename_namespace** принимает один аргумент — *newname*, который указывает новое имя для пространства имен.

Чтобы удалить пространство имен, используйте вместо него атрибут [no_namespace](../preprocessor/no-namespace.md) .

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
