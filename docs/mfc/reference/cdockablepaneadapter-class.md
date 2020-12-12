---
description: 'Дополнительные сведения о: Кдоккаблепанеадаптер Class'
title: Класс Кдоккаблепанеадаптер
ms.date: 11/04/2016
f1_keywords:
- CDockablePaneAdapter
- AFXDOCKABLEPANEADAPTER/CDockablePaneAdapter
- AFXDOCKABLEPANEADAPTER/CDockablePaneAdapter::GetWrappedWnd
- AFXDOCKABLEPANEADAPTER/CDockablePaneAdapter::LoadState
- AFXDOCKABLEPANEADAPTER/CDockablePaneAdapter::SaveState
- AFXDOCKABLEPANEADAPTER/CDockablePaneAdapter::SetWrappedWnd
helpviewer_keywords:
- CDockablePaneAdapter [MFC], GetWrappedWnd
- CDockablePaneAdapter [MFC], LoadState
- CDockablePaneAdapter [MFC], SaveState
- CDockablePaneAdapter [MFC], SetWrappedWnd
ms.assetid: 6ed6cf82-f39c-4d0c-bf7c-8641495cf8f3
ms.openlocfilehash: 0a46ef15d35194203d6e5c035555de0d80b63c72
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185041"
---
# <a name="cdockablepaneadapter-class"></a>Класс Кдоккаблепанеадаптер

Обеспечивает поддержку прикрепления производных панелей от `CWnd`.

## <a name="syntax"></a>Синтаксис

```
class CDockablePaneAdapter : public CDockablePane
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кдоккаблепанеадаптер:: Жетвраппедвнд](#getwrappedwnd)|Возвращает окно в оболочке.|
|[CDockablePaneAdapter::LoadState](#loadstate)|(Переопределяет [CDockablePane:: LoadState](cdockablepane-class.md#loadstate).)|
|[CDockablePaneAdapter::SaveState](#savestate)|(Переопределяет [CDockablePane:: SaveState](cdockablepane-class.md).)|
|[CDockablePaneAdapter::SetWrappedWnd](#setwrappedwnd)||

## <a name="remarks"></a>Комментарии

Как правило, платформа создает экземпляры объектов этого класса при использовании методов [CMFCBaseTabCtrl:: аддтаб](../../mfc/reference/cmfcbasetabctrl-class.md#addtab) или [CMFCBaseTabCtrl:: инсерттаб](../../mfc/reference/cmfcbasetabctrl-class.md#inserttab) .

Если вы хотите настроить `CDockablePaneAdapter` поведение, просто создайте производный от него новый класс и задайте в качестве сведений о классе среды выполнения окно с вкладками с помощью [CMFCBaseTabCtrl:: SetDockingBarWrapperRTC](../../mfc/reference/cmfcbasetabctrl-class.md#setdockingbarwrapperrtc).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)\
└ &nbsp; [От CCmdTarget](../../mfc/reference/ccmdtarget-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [CWnd](../../mfc/reference/cwnd-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [CBasePane](../../mfc/reference/cbasepane-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [CPane](../../mfc/reference/cpane-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [CDockablePane](../../mfc/reference/cdockablepane-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [Кдоккаблепанеадаптер](../../mfc/reference/cdockablepaneadapter-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксдоккаблепанеадаптер. h

## <a name="cdockablepaneadaptergetwrappedwnd"></a><a name="getwrappedwnd"></a> Кдоккаблепанеадаптер:: Жетвраппедвнд

Возвращает базовое окно для адаптера закрепляемой панели.

```
virtual CWnd* GetWrappedWnd() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на окно с оболочкой.

### <a name="remarks"></a>Комментарии

Используйте эту функцию для доступа к окну с оболочкой.

## <a name="cdockablepaneadapterloadstate"></a><a name="loadstate"></a> Кдоккаблепанеадаптер:: LoadState

Загружает состояние панели из реестра.

```
virtual BOOL LoadState(
    LPCTSTR lpszProfileName = NULL,
    int nIndex = -1,
    UINT uiID = (UINT) -1);
```

### <a name="parameters"></a>Параметры

*лпсзпрофиленаме*<br/>
окне Имя профиля.

*ниндекс*<br/>
окне Индекс профиля.

*uiID*<br/>
окне Идентификатор области.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdockablepaneadaptersavestate"></a><a name="savestate"></a> Кдоккаблепанеадаптер:: SaveState

Сохраняет состояние панели в реестре.

```
virtual BOOL SaveState(
    LPCTSTR lpszProfileName = NULL,
    int nIndex = -1,
    UINT uiID = (UINT) -1);
```

### <a name="parameters"></a>Параметры

*лпсзпрофиленаме*<br/>
окне Имя профиля.

*ниндекс*<br/>
окне Индекс профиля (по умолчанию используется идентификатор элемента управления окна).

*uiID*<br/>
окне Идентификатор области.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdockablepaneadaptersetwrappedwnd"></a><a name="setwrappedwnd"></a> Кдоккаблепанеадаптер:: Сетвраппедвнд

Задает базовое окно для адаптера закрепляемой панели.

```
virtual BOOL SetWrappedWnd(CWnd* pWnd);
```

### <a name="parameters"></a>Параметры

*Приводится*<br/>
окне Указатель на окно для адаптера панели, для которого необходимо выполнить перенос.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CDockablePane](../../mfc/reference/cdockablepane-class.md)
