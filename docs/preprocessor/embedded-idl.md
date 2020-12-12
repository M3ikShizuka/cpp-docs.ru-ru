---
description: 'Дополнительные сведения: embedded_idl атрибута импорта'
title: embedded_idl атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- embedded_idl
helpviewer_keywords:
- embedded_idl attribute
ms.assetid: f1c1c2e8-3872-4172-8795-8d1288a20452
ms.openlocfilehash: a56c6e664c082db4b6eac078b7133a1ead947d3d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97300597"
---
# <a name="embedded_idl-import-attribute"></a>embedded_idl атрибут импорта

**Блок, относящийся только к языку C++**

Указывает, записывается ли библиотека типов в `.tlh` файл с сохраненным кодом, сформированным атрибутом.

## <a name="syntax"></a>Синтаксис

> **#import** *Type-Library* **embedded_idl** [ **(** { **"emitidl"**  |  **"no_emitidl"** } **)** ]

### <a name="parameters"></a>Параметры

**emitidl**\
Сведения о типе, импортированные из *библиотеки типов* , находятся в IDL, созданном для проекта с атрибутами. Это поведение является значением по умолчанию и действует, если параметр не указан в `embedded_idl` .

**"no_emitidl"**\
Сведения о типе, импортированные из *библиотеки типов* , ОТСУТСТВУЮТ в IDL, созданном для проекта с атрибутами.

## <a name="example"></a>Пример

```cpp
// import_embedded_idl.cpp
// compile with: /LD
#include <windows.h>
[module(name="MyLib2")];
#import "\school\bin\importlib.tlb" embedded_idl("no_emitidl")
```

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
