---
description: 'Дополнительные сведения о: Кмессажемап Class'
title: Класс Кмессажемап
ms.date: 11/04/2016
f1_keywords:
- CMessageMap
- ATLWIN/ATL::CMessageMap
- ATLWIN/ATL::CMessageMap::ProcessWindowMessage
helpviewer_keywords:
- CMessageMap class
- message maps, ATL
- ATL, message handlers
ms.assetid: 1f97bc16-a8a0-4cf0-b90f-1778813a5c8e
ms.openlocfilehash: 90ecdc101071b84362d328558ff2e74cb9bbeb6b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141444"
---
# <a name="cmessagemap-class"></a>Класс Кмессажемап

Этот класс позволяет сопоставлению сообщений объекта иметь доступ к другому объекту.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class ATL_NO_VTABLE CMessageMap
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмессажемап::P Роцессвиндовмессаже](#processwindowmessage)|Обращается к схеме сообщений в `CMessageMap` классе, производном от.|

## <a name="remarks"></a>Комментарии

`CMessageMap` является абстрактным базовым классом, который разрешает доступ к сопоставлению сообщений объекта другому объекту. Чтобы объект мог предоставлять свои карты сообщений, его класс должен быть производным от `CMessageMap` .

В библиотеке ATL используется `CMessageMap` для поддержки цепочек в цепочке окон и динамической схемы сообщений. Например, любой класс, содержащий объект [кконтаинедвиндов](../../atl/reference/ccontainedwindowt-class.md) , должен быть производным от `CMessageMap` . Следующий код взят из примера [подизменения](https://github.com/Microsoft/VCSamples/tree/master/VC2008Samples/ATL/Controls/SubEdit) . С помощью [ккомконтрол](../../atl/reference/ccomcontrol-class.md) `CAtlEdit` класс автоматически является производным от `CMessageMap` .

[!code-cpp[NVC_ATL_Windowing#90](../../atl/codesnippet/cpp/cmessagemap-class_1.h)]

Так как автономное окно, `m_EditCtrl` , будет использовать схему сообщений в содержащем классе, `CAtlEdit` является производной от `CMessageMap` .

Дополнительные сведения о картах сообщений см. в разделе [схемы сообщений](../../atl/message-maps-atl.md) статьи "классы окон ATL".

## <a name="requirements"></a>Требования

**Заголовок:** atlwin. h

## <a name="cmessagemapprocesswindowmessage"></a><a name="processwindowmessage"></a> Кмессажемап::P Роцессвиндовмессаже

Обращается к схеме сообщений, идентифицируемой *двмсгмапид* , в `CMessageMap` классе, производном от.

```
virtual BOOL ProcessWindowMessage(
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam,
    LRESULT& lResult,
    DWORD dwMsgMapID) = 0;
```

### <a name="parameters"></a>Параметры

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

*двмсгмапид*<br/>
окне Идентификатор схемы сообщений, которая будет обрабатывать сообщение. Схема сообщений по умолчанию, объявленная с [BEGIN_MSG_MAP](message-map-macros-atl.md#begin_msg_map), определяется значением 0. Альтернативная схема сообщений, объявленная с помощью [ALT_MSG_MAP (мсгмапид)](message-map-macros-atl.md#alt_msg_map), определяется `msgMapID` .

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если сообщение полностью обработано; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Вызывается процедурой окна объекта [кконтаинедвиндов](../../atl/reference/ccontainedwindowt-class.md) или объекта, динамически сцепленного с картой сообщений.

## <a name="see-also"></a>См. также раздел

[Класс Кдинамикчаин](../../atl/reference/cdynamicchain-class.md)<br/>
[BEGIN_MSG_MAP](message-map-macros-atl.md#begin_msg_map)<br/>
[ALT_MSG_MAP (Мсгмапид)](message-map-macros-atl.md#alt_msg_map)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
