---
description: 'Дополнительные сведения о: модели потоков и классы критических разделов'
title: Модели потоков и классы критических секций (ATL)
ms.date: 11/04/2016
helpviewer_keywords:
- ATL, critical sections
- ATL, multithreading
- threading [ATL], models
- critical sections
ms.assetid: 759f05ef-6285-4be6-a2cc-78572dd75146
ms.openlocfilehash: 51ad5a5f2f03bfe080395966d0c480615c49a109
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97138285"
---
# <a name="threading-models-and-critical-sections-classes"></a>Классы потоковой модели и критические разделы

Следующие классы определяют потоковую модель и критическую секцию:

- [Катлаутосреадмодуле](../atl/reference/catlautothreadmodule-class.md) Реализует COM-сервер модели подразделения в пуле потоков.

- [Катлаутосреадмодулет](../atl/reference/catlautothreadmodulet-class.md) Предоставляет методы для реализации COM-сервера модели подразделения в пуле потоков.

- [Ккоммултисреадмодел](../atl/reference/ccommultithreadmodel-class.md) Предоставляет потокобезопасные методы для увеличения и уменьшения переменной. Предоставляет критическую секцию.

- [Ккоммултисреадмоделнокс](../atl/reference/ccommultithreadmodelnocs-class.md) Предоставляет потокобезопасные методы для увеличения и уменьшения переменной. Не предоставляет критическую секцию.

- [Ккомсинглесреадмодел](../atl/reference/ccomsinglethreadmodel-class.md) Предоставляет методы для увеличения и уменьшения переменной. Не предоставляет критическую секцию.

- [Ккомобжектсреадмодел](../atl/reference/atl-typedefs.md#ccomobjectthreadmodel) Определяет соответствующий класс потоковой модели для одного класса объекта.

- [Ккомглобалссреадмодел](../atl/reference/atl-typedefs.md#ccomglobalsthreadmodel) Определяет соответствующий класс потоковой модели для глобально доступного объекта.

- [Ккомаутокритикалсектион](../atl/reference/ccomautocriticalsection-class.md) Содержит методы для получения и освобождения критического раздела. Критическая секция автоматически инициализируется.

- [Ккомкритикалсектион](../atl/reference/ccomcriticalsection-class.md) Содержит методы для получения и освобождения критического раздела. Критическая секция должна быть явно инициализирована.

- [Ккомфакекритикалсектион](../atl/reference/ccomfakecriticalsection-class.md) Отражает методы в `CComCriticalSection` без предоставления критической секции. Методы в `CComFakeCriticalSection` не выполняют никаких действий.

- [Кртсреадтраитс](../atl/reference/crtthreadtraits-class.md) Предоставляет функцию создания для потока CRT. Используйте этот класс, если поток будет использовать функции CRT.

- [Win32ThreadTraits](../atl/reference/win32threadtraits-class.md) Предоставляет функцию создания для потока Windows. Используйте этот класс, если поток не будет использовать функции CRT.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../atl/atl-class-overview.md)
