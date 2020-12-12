---
description: 'Дополнительные сведения о: Кмфкриббонлинкктрл Class'
title: Класс Кмфкриббонлинкктрл
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonLinkCtrl
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::CMFCRibbonLinkCtrl
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::CopyFrom
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::GetCompactSize
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::GetLink
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::GetRegularSize
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::GetToolTipText
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::IsDrawTooltipImage
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::OnDraw
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::OnDrawMenuImage
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::OnMouseMove
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::OnSetIcon
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::OpenLink
- AFXRIBBONLINKCTRL/CMFCRibbonLinkCtrl::SetLink
helpviewer_keywords:
- CMFCRibbonLinkCtrl [MFC], CMFCRibbonLinkCtrl
- CMFCRibbonLinkCtrl [MFC], CopyFrom
- CMFCRibbonLinkCtrl [MFC], GetCompactSize
- CMFCRibbonLinkCtrl [MFC], GetLink
- CMFCRibbonLinkCtrl [MFC], GetRegularSize
- CMFCRibbonLinkCtrl [MFC], GetToolTipText
- CMFCRibbonLinkCtrl [MFC], IsDrawTooltipImage
- CMFCRibbonLinkCtrl [MFC], OnDraw
- CMFCRibbonLinkCtrl [MFC], OnDrawMenuImage
- CMFCRibbonLinkCtrl [MFC], OnMouseMove
- CMFCRibbonLinkCtrl [MFC], OnSetIcon
- CMFCRibbonLinkCtrl [MFC], OpenLink
- CMFCRibbonLinkCtrl [MFC], SetLink
ms.assetid: 77ae1941-e0ab-4a9d-911e-1752d34c079b
ms.openlocfilehash: 19b10643fa1af25dae4a5dc888f61d1c9ecaaee7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321791"
---
# <a name="cmfcribbonlinkctrl-class"></a>Класс Кмфкриббонлинкктрл

Реализует гиперссылку, которая расположена на ленте. Гиперссылка при щелчке открывает веб-страницу.
Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonLinkCtrl : public CMFCRibbonButton
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonLinkCtrl::CMFCRibbonLinkCtrl](#cmfcribbonlinkctrl)|Создает и инициализирует объект `CMFCRibbonLinkCtrl`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonLinkCtrl::CopyFrom](#copyfrom)|(Переопределяет `CMFCRibbonButton::CopyFrom`.)|
|[CMFCRibbonLinkCtrl::GetCompactSize](#getcompactsize)|(Переопределяет [CMFCRibbonButton:: жеткомпактсизе](../../mfc/reference/cmfcribbonbutton-class.md#getcompactsize).)|
|[CMFCRibbonLinkCtrl::GetLink](#getlink)|Возвращает значение гиперссылки.|
|[CMFCRibbonLinkCtrl::GetRegularSize](#getregularsize)|(Переопределяет [CMFCRibbonButton:: жетрегуларсизе](../../mfc/reference/cmfcribbonbutton-class.md#getregularsize).)|
|[CMFCRibbonLinkCtrl::GetToolTipText](#gettooltiptext)|(Переопределяет [CMFCRibbonButton:: жеттултиптекст](../../mfc/reference/cmfcribbonbutton-class.md#gettooltiptext).)|
|[CMFCRibbonLinkCtrl::IsDrawTooltipImage](#isdrawtooltipimage)|(Переопределяет `CMFCRibbonButton::IsDrawTooltipImage`.)|
|[CMFCRibbonLinkCtrl::OnDraw](#ondraw)|(Переопределяет [CMFCRibbonButton:: OnDraw](../../mfc/reference/cmfcribbonbutton-class.md#ondraw).)|
|[CMFCRibbonLinkCtrl::OnDrawMenuImage](#ondrawmenuimage)|(Переопределяет [метод CMFCRibbonBaseElement:: ондравменуимаже](../../mfc/reference/cmfcribbonbaseelement-class.md#ondrawmenuimage).)|
|[CMFCRibbonLinkCtrl::OnMouseMove](#onmousemove)|(Переопределяет `CMFCRibbonButton::OnMouseMove`.)|
|[CMFCRibbonLinkCtrl::OnSetIcon](#onseticon)||
|[CMFCRibbonLinkCtrl::OpenLink](#openlink)|Открывает веб-страницу, указанную в гиперссылке.|
|[CMFCRibbonLinkCtrl::SetLink](#setlink)|Задает значение гиперссылки.|

## <a name="remarks"></a>Комментарии

После создания гиперссылки добавьте ее на панель, вызвав [CMFCRibbonPanel:: Add](../../mfc/reference/cmfcribbonpanel-class.md#add).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)\
└ &nbsp; [Метод CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [Кмфкриббонлинкктрл](../../mfc/reference/cmfcribbonlinkctrl-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонлинкктрл. h

## <a name="cmfcribbonlinkctrlcmfcribbonlinkctrl"></a><a name="cmfcribbonlinkctrl"></a> Кмфкриббонлинкктрл:: Кмфкриббонлинкктрл

Создает и инициализирует объект [кмфкриббонлинкктрл](../../mfc/reference/cmfcribbonlinkctrl-class.md) .

```
CMFCRibbonLinkCtrl(
    UINT nID,
    LPCTSTR lpszText,
    LPCTSTR lpszLink);
```

### <a name="parameters"></a>Параметры

*nID*<br/>
окне Указывает идентификатор команды, которая выполняется при нажатии на элемент управления Link.

*lpszText*<br/>
окне Задает метку, отображаемую на элементе управления ссылки.

*лпсзлинк*<br/>
окне Задает гиперссылку, связанную с элементом управления "ссылка".

### <a name="example"></a>Пример

В следующем примере показано, как использовать конструктор `CMFCRibbonLinkCtrl` класса. Этот фрагмент кода является частью [примера мини-приложений ленты](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_RibbonGadgets#1](../../mfc/reference/codesnippet/cpp/cmfcribbonlinkctrl-class_1.cpp)]

## <a name="cmfcribbonlinkctrlcopyfrom"></a><a name="copyfrom"></a> Кмфкриббонлинкктрл:: CopyFrom

```
virtual void CopyFrom(const CMFCRibbonBaseElement& src);
```

### <a name="parameters"></a>Параметры

окне *src*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlgetcompactsize"></a><a name="getcompactsize"></a> Кмфкриббонлинкктрл:: Жеткомпактсизе

```
virtual CSize GetCompactSize(CDC* pDC);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlgetlink"></a><a name="getlink"></a> Кмфкриббонлинкктрл::.

Возвращает значение гиперссылки.

```
LPCTSTR GetLink() const;
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение гиперссылки.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlgetregularsize"></a><a name="getregularsize"></a> Кмфкриббонлинкктрл:: Жетрегуларсизе

```
virtual CSize GetRegularSize(CDC* pDC);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlgettooltiptext"></a><a name="gettooltiptext"></a> Кмфкриббонлинкктрл:: Жеттултиптекст

```
virtual CString GetToolTipText() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlondrawmenuimage"></a><a name="ondrawmenuimage"></a> Кмфкриббонлинкктрл:: Ондравменуимаже

```
virtual BOOL OnDrawMenuImage(CDC*, CRect);
```

### <a name="parameters"></a>Параметры

окне *&#42;CDC*<br/>
окне *Крект*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlisdrawtooltipimage"></a><a name="isdrawtooltipimage"></a> Кмфкриббонлинкктрл:: Исдравтултипимаже

```
virtual BOOL IsDrawTooltipImage() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlondraw"></a><a name="ondraw"></a> Кмфкриббонлинкктрл:: OnDraw

```
virtual void OnDraw(CDC* pDC);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlonmousemove"></a><a name="onmousemove"></a> Кмфкриббонлинкктрл:: OnMouseMove

```
virtual void OnMouseMove(CPoint point);
```

### <a name="parameters"></a>Параметры

окне *точка*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlonseticon"></a><a name="onseticon"></a> Кмфкриббонлинкктрл:: Онсетикон

```
virtual void OnSetIcon();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonlinkctrlopenlink"></a><a name="openlink"></a> Кмфкриббонлинкктрл:: Опенлинк

Открывает веб-страницу, указанную в гиперссылке.

```
BOOL OpenLink();
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если связанная веб-страница успешно открыта. в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Открывает веб-страницу, используя гиперссылку, связанную с `CMFCRibbonLinkCtrl` объектом.

## <a name="cmfcribbonlinkctrlsetlink"></a><a name="setlink"></a> Кмфкриббонлинкктрл:: Сетлинк

Задает значение гиперссылки.

```cpp
void SetLink(LPCTSTR lpszLink);
```

### <a name="parameters"></a>Параметры

*лпсзлинк*<br/>
окне Задает текст гиперссылки.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)
