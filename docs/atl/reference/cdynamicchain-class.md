---
description: 'Дополнительные сведения о: Кдинамикчаин Class'
title: Класс Кдинамикчаин
ms.date: 11/04/2016
f1_keywords:
- CDynamicChain
- ATLWIN/ATL::CDynamicChain
- ATLWIN/ATL::CDynamicChain::CDynamicChain
- ATLWIN/ATL::CDynamicChain::CallChain
- ATLWIN/ATL::CDynamicChain::RemoveChainEntry
- ATLWIN/ATL::CDynamicChain::SetChainEntry
helpviewer_keywords:
- message maps, chaining
- chaining message maps
- CDynamicChain class
ms.assetid: f084b2be-0e77-4836-973d-ae278a1e9da8
ms.openlocfilehash: 5ada99b519900150afa2143fb1527245797fed98
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141821"
---
# <a name="cdynamicchain-class"></a>Класс Кдинамикчаин

Этот класс предоставляет методы, поддерживающие динамическую цепочку сопоставлений сообщений.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CDynamicChain
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кдинамикчаин:: Кдинамикчаин](#cdynamicchain)|Конструктор.|
|[Кдинамикчаин:: ~ Кдинамикчаин](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кдинамикчаин:: Каллчаин](#callchain)|Направляет сообщение Windows в схему сообщений другого объекта.|
|[Кдинамикчаин:: Ремовечаинентри](#removechainentry)|Удаляет запись схемы сообщений из коллекции.|
|[Кдинамикчаин:: Сетчаинентри](#setchainentry)|Добавляет запись схемы сообщения в коллекцию или изменяет существующую запись.|

## <a name="remarks"></a>Комментарии

`CDynamicChain` Управляет коллекцией схем сообщений, позволяя пересылать сообщения Windows во время выполнения в схему сообщений другого объекта.

Чтобы добавить поддержку динамической цепочки схем сообщений, выполните следующие действия.

- Создайте класс, производный от `CDynamicChain` . В схеме сообщений укажите макрос [CHAIN_MSG_MAP_DYNAMIC](message-map-macros-atl.md#chain_msg_map_dynamic) , чтобы связать его с картой сообщений другого объекта по умолчанию.

- Создайте производный класс от [кмессажемап](../../atl/reference/cmessagemap-class.md)для каждого класса, к которому необходимо создать цепочку. `CMessageMap` позволяет объекту предоставлять свои карты сообщений другим объектам.

- Вызовите метод `CDynamicChain::SetChainEntry` , чтобы выяснить, к какому объекту и какому сопоставлению следует привязать цепочку сообщений.

Например, предположим, что ваш класс определен следующим образом:

[!code-cpp[NVC_ATL_Windowing#88](../../atl/codesnippet/cpp/cdynamicchain-class_1.h)]

Затем клиент вызывает `CMyWindow::SetChainEntry` :

[!code-cpp[NVC_ATL_Windowing#89](../../atl/codesnippet/cpp/cdynamicchain-class_2.cpp)]

где `chainedObj` — это связанный объект, который является экземпляром класса, производного от `CMessageMap` . Теперь, если `myCtl` получает сообщение, которое не обрабатывается `OnPaint` или `OnSetFocus` , то процедура окна направляет сообщение в `chainedObj` схему сообщений по умолчанию.

Дополнительные сведения о цепочке схем сообщений см. в разделе [схемы сообщений](../../atl/message-maps-atl.md) статьи "классы окон ATL".

## <a name="requirements"></a>Требования

**Заголовок:** atlwin. h

## <a name="cdynamicchaincallchain"></a><a name="callchain"></a> Кдинамикчаин:: Каллчаин

Направляет сообщение Windows в схему сообщений другого объекта.

```
BOOL CallChain(
    DWORD dwChainID,
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam,
    LRESULT& lResult);
```

### <a name="parameters"></a>Параметры

*двчаинид*<br/>
окне Уникальный идентификатор, связанный с сцепленным объектом и его картой сообщений.

*hWnd*<br/>
окне Маркер окна, получающего сообщение.

*Uiacp*<br/>
окне Сообщение, отправленное в окно.

*wParam*<br/>
окне Дополнительные сведения, относящиеся к конкретному сообщению.

*lParam*<br/>
окне Дополнительные сведения, относящиеся к конкретному сообщению.

*lResult*<br/>
заполняет Результат обработки сообщения.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если сообщение полностью обработано; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Для вызова процедуры окна `CallChain` необходимо указать макрос [CHAIN_MSG_MAP_DYNAMIC](message-map-macros-atl.md#chain_msg_map_dynamic) в схеме сообщений. Пример см. в обзоре [кдинамикчаин](../../atl/reference/cdynamicchain-class.md) .

`CallChain` требуется предыдущий вызов [сетчаинентри](#setchainentry) для связывания значения *двчаинид* с объектом и его картой сообщений.

## <a name="cdynamicchaincdynamicchain"></a><a name="cdynamicchain"></a> Кдинамикчаин:: Кдинамикчаин

Конструктор.

```
CDynamicChain();
```

## <a name="cdynamicchaincdynamicchain"></a><a name="dtor"></a> Кдинамикчаин:: ~ Кдинамикчаин

Деструктор

```
~CDynamicChain();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы.

## <a name="cdynamicchainremovechainentry"></a><a name="removechainentry"></a> Кдинамикчаин:: Ремовечаинентри

Удаляет указанную схему сообщений из коллекции.

```
BOOL RemoveChainEntry(DWORD dwChainID);
```

### <a name="parameters"></a>Параметры

*двчаинид*<br/>
окне Уникальный идентификатор, связанный с сцепленным объектом и его картой сообщений. Первоначально это значение определяется с помощью вызова [сетчаинентри](#setchainentry).

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если схема сообщения успешно удалена из коллекции. В противном случае — значение FALSE.

## <a name="cdynamicchainsetchainentry"></a><a name="setchainentry"></a> Кдинамикчаин:: Сетчаинентри

Добавляет указанную схему сообщения в коллекцию.

```
BOOL SetChainEntry(
    DWORD dwChainID,
    CMessageMap* pObject,
    DWORD dwMsgMapID = 0);
```

### <a name="parameters"></a>Параметры

*двчаинид*<br/>
окне Уникальный идентификатор, связанный с сцепленным объектом и его картой сообщений.

*Объект*<br/>
окне Указатель на связанный объект, объявляющий схему сообщения. Этот объект должен быть производным от [кмессажемап](../../atl/reference/cmessagemap-class.md).

*двмсгмапид*<br/>
окне Идентификатор схемы сообщений в связанном объекте. Значение по умолчанию — 0, которое определяет схему сообщений по умолчанию, объявленную с помощью [BEGIN_MSG_MAP](message-map-macros-atl.md#begin_msg_map). Чтобы указать альтернативную схему сообщения, объявленную с помощью [ALT_MSG_MAP (мсгмапид)](message-map-macros-atl.md#alt_msg_map), передайте `msgMapID` .

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если схема сообщения успешно добавлена в коллекцию. В противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Если значение *двчаинид* уже существует в коллекции, связанный объект и схема сообщения заменяются *объект* и *двмсгмапид* соответственно. В противном случае добавляется новая запись.

## <a name="see-also"></a>См. также раздел

[Класс Квиндовимпл](../../atl/reference/cwindowimpl-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
