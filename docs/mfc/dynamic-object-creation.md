---
description: 'Дополнительные сведения: динамическое создание объектов'
title: Динамическое создание объектов
ms.date: 03/27/2020
helpviewer_keywords:
- object creation [MFC], dynamically at run time
- CObject class [MFC], dynamic object creation
- objects [MFC], creating dynamically at run time
- dynamic object creation [MFC]
ms.assetid: 3e0f51cb-3e24-4231-817f-1c0ce9f2d5df
ms.openlocfilehash: b39c0561a98807030c471b3de4cd5921883f9f0e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97290977"
---
# <a name="dynamic-object-creation"></a>Динамическое создание объектов

В этой статье объясняется, как динамически создать объект во время выполнения. Процедура использует сведения о классе времени выполнения, как описано в статье [доступ к Run-Time сведениям о классе](accessing-run-time-class-information.md).

#### <a name="dynamically-create-an-object-given-its-run-time-class"></a>Динамическое создание объекта по заданному классу времени выполнения

1. Используйте следующий код для динамического создания объекта с помощью `CreateObject` функции `CRuntimeClass` . При сбое `CreateObject` возвращает **значение NULL** вместо того, чтобы вызывать исключение:

   [!code-cpp[NVC_MFCCObjectSample#6](codesnippet/cpp/dynamic-object-creation_1.cpp)]

## <a name="see-also"></a>См. также раздел

[Уничтожение объектов Window](tn017-destroying-window-objects.md) 
 [Использование CObject](using-cobject.md)
