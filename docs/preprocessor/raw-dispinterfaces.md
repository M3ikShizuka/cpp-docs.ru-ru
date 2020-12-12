---
description: 'Дополнительные сведения: raw_dispinterfaces атрибута импорта'
title: raw_dispinterfaces атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- raw_dispinterfaces
helpviewer_keywords:
- raw_dispinterfaces attribute
ms.assetid: f762864d-29bf-445b-825a-ba7b29a95409
ms.openlocfilehash: 447f76bdee16d2719c02ad4a73883f8f176f2584
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202019"
---
# <a name="raw_dispinterfaces-import-attribute"></a>raw_dispinterfaces атрибут импорта

**Блок, относящийся только к языку C++**

Указывает компилятору создавать низкоуровневые функции оболочки для методов disp-интерфейсов, а также для свойств, которые вызывают `IDispatch::Invoke` и возвращают код ошибки HRESULT.

## <a name="syntax"></a>Синтаксис

> **raw_dispinterfaces** типов **#import** *-Library*

## <a name="remarks"></a>Комментарии

Если этот атрибут не указан, создаются только высокоуровневые оболочки, которые вызывают исключения C++ в случае сбоя.

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
