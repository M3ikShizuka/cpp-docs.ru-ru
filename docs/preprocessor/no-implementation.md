---
description: 'Дополнительные сведения: no_implementation атрибута импорта'
title: no_implementation атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- no_implementation
helpviewer_keywords:
- no_implementation attribute
ms.assetid: bdc67785-e131-409c-87bc-f4d2f4abb07b
ms.openlocfilehash: 0cfd51b344847d2e5658fd4e4ec1a9f30db51fe6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333323"
---
# <a name="no_implementation-import-attribute"></a>no_implementation атрибут импорта

**Блок, относящийся только к языку C++**

Подавляет создание `.tli` заголовка, содержащего реализации функций-членов-оболочек.

## <a name="syntax"></a>Синтаксис

> **no_implementation** типов **#import** *-Library*

## <a name="remarks"></a>Комментарии

Если этот атрибут указан, то `.tlh` заголовок с объявлениями, которые предоставляют элементы библиотеки типов, будет создан без `#include` инструкции для включения `.tli` файла заголовка.

Этот атрибут используется в сочетании с [implementation_only](../preprocessor/implementation-only.md).

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
