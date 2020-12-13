---
description: 'Дополнительные сведения: no_dual_interfaces атрибута импорта'
title: no_dual_interfaces атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- no_dual_interfaces
helpviewer_keywords:
- no_dual_interfaces attribute
ms.assetid: 9acd5d9d-4a49-4cdc-9470-73a2c23cf512
ms.openlocfilehash: 1c3010b252ac71e38312fa193520938fbb4d681a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333340"
---
# <a name="no_dual_interfaces-import-attribute"></a>no_dual_interfaces атрибут импорта

**Блок, относящийся только к языку C++**

Изменяет способ, которым компилятор создает функции оболочки для методов сдвоенных интерфейсов.

## <a name="syntax"></a>Синтаксис

> **no_dual_interfaces** типов **#import** *-Library*

## <a name="remarks"></a>Комментарии

Как правило, обертка вызывает метод через таблицу виртуальной функции для интерфейса. При использовании **no_dual_interfaces** оболочка вызывает `IDispatch::Invoke` метод для вызова метода.

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
