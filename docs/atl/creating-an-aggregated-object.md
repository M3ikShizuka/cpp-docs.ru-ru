---
description: 'Дополнительные сведения: создание агрегированного объекта'
title: Создание агрегированного объекта
ms.date: 11/04/2016
helpviewer_keywords:
- aggregation [C++], creating aggregated objects
- aggregate objects [C++], creating
ms.assetid: fc29d7aa-fd53-4276-9c2f-37379f71b179
ms.openlocfilehash: e6efbf63e28d0477730a2d7c31ec91e9b75520e4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97153230"
---
# <a name="creating-an-aggregated-object"></a>Создание агрегированного объекта

Вызовы делегатов агрегирования `IUnknown` предоставляют указатель на внешний объект `IUnknown` во внутреннем объекте.

## <a name="to-create-an-aggregated-object"></a>Создание агрегированного объекта

1. Добавьте `IUnknown` указатель на объект класса и инициализируйте его значением NULL в конструкторе.

1. Переопределите [финалконструкт](../atl/reference/ccomobjectrootex-class.md#finalconstruct) , чтобы создать статистическое выражение.

1. Используйте `IUnknown` указатель, определенный в шаге 1, в качестве второго параметра для макросов [COM_INTERFACE_ENTRY_AGGREGATE](reference/com-interface-entry-macros.md#com_interface_entry_aggregate) .

1. Переопределите [финалрелеасе](../atl/reference/ccomobjectrootex-class.md#finalrelease) , чтобы освободить `IUnknown` указатель.

> [!NOTE]
> Если вы используете и выпустите интерфейс из агрегированного объекта во время `FinalConstruct` , добавьте макрос [DECLARE_PROTECT_FINAL_CONSTRUCT](reference/aggregation-and-class-factory-macros.md#declare_protect_final_construct) в определение объекта класса.

## <a name="see-also"></a>См. также раздел

[Основы COM-объектов ATL](../atl/fundamentals-of-atl-com-objects.md)
