---
description: 'Дополнительные сведения о: использование IDispEventSimpleImpl'
title: Использование IDispEventSimpleImpl (ATL)
ms.date: 08/19/2019
helpviewer_keywords:
- IDispEventSimpleImpl class, using
ms.assetid: 8640ad1a-4bd0-40a5-b5e4-7322685d7aab
ms.openlocfilehash: c0b3f6a0ecdcaae084d3f5d62c19745ee15ac6e9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97138168"
---
# <a name="using-idispeventsimpleimpl"></a>Использование IDispEventSimpleImpl

При использовании `IDispEventSimpleImpl` для работы с событиями необходимо выполнить следующие действия:

- Создайте класс, производный от [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md).

- Добавьте карту приемника событий в класс.

- Определите [_ATL_FUNC_INFO](../atl/reference/atl-func-info-structure.md) структуры, описывающие события.

- Добавьте записи в карту приемника событий с помощью макроса [SINK_ENTRY_INFO](reference/composite-control-macros.md#sink_entry_info) .

- Реализуйте методы, которые вы заинтересованы в обработке.

- Посоветовать и порекомендовать источник событий.

## <a name="example"></a>Пример

В приведенном ниже примере показано, как управлять `DocumentChange` событием, запущенным объектом **приложения** Word. Это событие определяется как метод в `ApplicationEvents` DISP-интерфейсе.

Пример приведен в примере [атлевенсандлинг](../overview/visual-cpp-samples.md).

```cpp
[ uuid(000209F7-0000-0000-C000-000000000046), hidden ]
dispinterface ApplicationEvents {
properties:
methods:
    [id(0x00000001), restricted, hidden]
    void Startup();

    [id(0x00000002)]
    void Quit();

    [id(0x00000003)]
    void DocumentChange();
};
```

В примере используется `#import` для создания необходимых файлов заголовков из библиотеки типов Word. Если вы хотите использовать этот пример с другими версиями Word, необходимо указать правильный DLL-файл Mso. Например, Office 2000 предоставляет mso.dll mso9.dll и Оффицексп. Этот код упрощен из *PCH. h* (*stdafx. h* в Visual Studio 2017 и более ранних версиях):

[!code-cpp[NVC_ATL_EventHandlingSample#1](../atl/codesnippet/cpp/using-idispeventsimpleimpl_1.h)]

Единственной информацией из библиотеки типов, которая фактически используется в этом примере, является CLSID `Application` объекта Word и IID `ApplicationEvents` интерфейса. Эти сведения используются только во время компиляции.

Следующий код отображается в Simple. h. Соответствующий код отмечается комментариями:

[!code-cpp[NVC_ATL_EventHandlingSample#3](../atl/codesnippet/cpp/using-idispeventsimpleimpl_2.h)]

Ниже приведен код из простого cpp-кода:

[!code-cpp[NVC_ATL_EventHandlingSample#4](../atl/codesnippet/cpp/using-idispeventsimpleimpl_3.cpp)]

## <a name="see-also"></a>См. также раздел

[Обработка событий](../atl/event-handling-and-atl.md)<br/>
[Пример Атлевенсандлинг](../overview/visual-cpp-samples.md)
