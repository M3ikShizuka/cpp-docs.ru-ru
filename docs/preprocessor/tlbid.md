---
description: 'Дополнительные сведения о: тлбид Import Attribute'
title: тлбид, атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- tlbid
helpviewer_keywords:
- tlbid attribute
ms.assetid: 54b06785-191b-4e77-a9a5-485f2b4acb09
ms.openlocfilehash: 9bbf15f64c1813013fcd839a2d4f0a34c9872aff
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339049"
---
# <a name="tlbid-import-attribute"></a>тлбид, атрибут импорта

**Блок, относящийся только к языку C++**

Позволяет загружать библиотеки, отличные от основной библиотеки типов.

## <a name="syntax"></a>Синтаксис

> **#import** *Type-Library-DLL* **тлбид (** *число* **)**

### <a name="parameters"></a>Параметры

*Нумерация*\
Номер библиотеки типов в *Type-Library-DLL*.

## <a name="remarks"></a>Комментарии

Если в одну библиотеку DLL встроено несколько библиотек типов, можно загрузить библиотеки, отличные от первичной библиотеки типов, с помощью **тлбид**.

Пример:

```cpp
#import <MyResource.dll> tlbid(2)
```

эквивалентно правилу

```cpp
LoadTypeLib("MyResource.dll\\2");
```

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
