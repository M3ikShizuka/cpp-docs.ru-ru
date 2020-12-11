---
description: 'Дополнительные сведения: несколько сдвоенных интерфейсов'
title: Несколько сдвоенных интерфейсов
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- multiple dual interfaces
- COM_INTERFACE_ENTRY2 macro
- dual interfaces, exposing multiple
- multiple dual interfaces, exposing with ATL
- IDispatchImpl class, multiple dual interfaces
- COM_INTERFACE_ENTRY_IID macro
ms.assetid: 7fea86e6-247f-4063-be6e-85588a9e3719
ms.openlocfilehash: d90c0176b3165cc0e5b976a29ec58b58fd3a7a56
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97159419"
---
# <a name="multiple-dual-interfaces"></a>Несколько сдвоенных интерфейсов

Можно сочетать преимущества двойного интерфейса (то есть гибкость как таблицы vtable, так и позднего связывания, делая его доступным для языков сценариев, а также для C++) с помощью методов множественного наследования.

Хотя можно предоставить несколько сдвоенных интерфейсов для одного COM-объекта, делать это не рекомендуется. При наличии нескольких сдвоенных интерфейсов должен быть предоставлен только один `IDispatch` интерфейс. Методы, позволяющие убедиться в том, что в этом случае применяются такие штрафы, как утрата функции или повышение сложности кода. Разработчик, который рассматривал этот подход, должен тщательно взвесить преимущества и недостатки.

## <a name="exposing-a-single-idispatch-interface"></a>Предоставление доступа к одному интерфейсу IDispatch

Можно предоставить несколько сдвоенных интерфейсов для одного объекта, производя от двух или более специализаций `IDispatchImpl` . Однако, если разрешить клиентам запрашивать `IDispatch` интерфейс, необходимо использовать макрос [COM_INTERFACE_ENTRY2](reference/com-interface-entry-macros.md#com_interface_entry2) (или [COM_INTERFACE_ENTRY_IID](reference/com-interface-entry-macros.md#com_interface_entry_iid))), чтобы указать, какой базовый класс следует использовать для реализации `IDispatch` .

[!code-cpp[NVC_ATL_COM#23](../atl/codesnippet/cpp/multiple-dual-interfaces_1.h)]

Поскольку предоставляется только один `IDispatch` интерфейс, клиенты, которые могут обращаться к вашим объектам только через `IDispatch` интерфейс, не смогут получить доступ к методам или свойствам в любом другом интерфейсе.

## <a name="combining-multiple-dual-interfaces-into-a-single-implementation-of-idispatch"></a>Объединение нескольких сдвоенных интерфейсов в одну реализацию IDispatch

В библиотеке ATL не предусмотрена поддержка объединения нескольких сдвоенных интерфейсов в одну реализацию `IDispatch` . Однако существует несколько известных подходов к ручному объединению интерфейсов, таких как создание шаблонного класса, содержащего объединение отдельных `IDispatch` интерфейсов, создание нового объекта для выполнения `QueryInterface` функции или использование реализации вложенных объектов, основанной на TypeInfo, для создания `IDispatch` интерфейса.

Эти подходы имеют проблемы с потенциальными конфликтами пространств имен, а также сложность кода и удобство обслуживания. Не рекомендуется создавать несколько сдвоенных интерфейсов.

## <a name="see-also"></a>См. также раздел

[Сдвоенные интерфейсы и ATL](../atl/dual-interfaces-and-atl.md)
