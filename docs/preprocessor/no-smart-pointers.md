---
description: 'Дополнительные сведения: no_smart_pointers атрибута импорта'
title: no_smart_pointers атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- no_smart_pointers
helpviewer_keywords:
- no_smart_pointers attribute
ms.assetid: d69dd71e-08a8-4446-a3d0-a062dc29cb17
ms.openlocfilehash: cf2299668a2e1b24cdf45069766466f448ee9d66
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333276"
---
# <a name="no_smart_pointers-import-attribute"></a>no_smart_pointers атрибут импорта

**Блок, относящийся только к языку C++**

Отключает создание интеллектуальных указателей для всех интерфейсов в библиотеке типов.

## <a name="syntax"></a>Синтаксис

> **no_smart_pointers** типов **#import** *-Library*

## <a name="remarks"></a>Комментарии

По умолчанию при использовании директивы `#import` пользователь получает объявление интеллектуального указателя для всех интерфейсов в библиотеке типов. Эти смарт-указатели имеют тип [_com_ptr_t](../cpp/com-ptr-t-class.md).

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
