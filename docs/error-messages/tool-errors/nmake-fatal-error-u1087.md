---
description: 'Дополнительные сведения: Неустранимая ошибка NMAKE U1087'
title: Неустранимая ошибка NMAKE U1087
ms.date: 11/04/2016
f1_keywords:
- U1087
helpviewer_keywords:
- U1087
ms.assetid: 5236ab54-e117-484d-99c3-852b061fd3d0
ms.openlocfilehash: 70b9254f04b0e0042da835e7482b4f0314224b01
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97345372"
---
# <a name="nmake-fatal-error-u1087"></a>Неустранимая ошибка NMAKE U1087

не может иметь: и:: зависимые объекты для одного и того же целевого объекта

Целевой объект не может быть указан одновременно в зависимости с одним двоеточием (**:**) и двойным двоеточием ( `::` ).

Чтобы указать целевой объект в нескольких блоках описания, используйте `::` в каждой строке зависимости.
