---
description: 'Дополнительные сведения о: CHtmlEditView Class'
title: Класс CHtmlEditView
ms.date: 11/04/2016
f1_keywords:
- CHtmlEditView
- AFXHTML/CHtmlEditView
- AFXHTML/CHtmlEditView::CHtmlEditView
- AFXHTML/CHtmlEditView::Create
- AFXHTML/CHtmlEditView::GetDHtmlDocument
- AFXHTML/CHtmlEditView::GetStartDocument
helpviewer_keywords:
- CHtmlEditView [MFC], CHtmlEditView
- CHtmlEditView [MFC], Create
- CHtmlEditView [MFC], GetDHtmlDocument
- CHtmlEditView [MFC], GetStartDocument
ms.assetid: 166c8ba8-3fb5-4dd7-a9ea-5bca662d00f6
ms.openlocfilehash: 9ab998ca16a26fd4ef7a23e4dc58c6542ec330b3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97261324"
---
# <a name="chtmleditview-class"></a>Класс CHtmlEditView

Предоставляет функции платформы редактирования WebBrowser в контексте архитектуры документов или представлений MFC.

## <a name="syntax"></a>Синтаксис

```
class CHtmlEditView : public CHtmlView, public CHtmlEditCtrlBase<CHtmlEditView>
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CHtmlEditView:: CHtmlEditView](#chtmleditview)|Формирует объект `CHtmlEditView`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CHtmlEditView:: Create](#create)|Создает новый объект Window.|
|[CHtmlEditView:: Жетдхтмлдокумент](#getdhtmldocument)|Возвращает `IHTMLDocument2` интерфейс текущего документа.|
|[CHtmlEditView:: Жетстартдокумент](#getstartdocument)|Возвращает имя документа по умолчанию для этого представления.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CView](../../mfc/reference/cview-class.md)

[CScrollView](../../mfc/reference/cscrollview-class.md)

[CFormView](../../mfc/reference/cformview-class.md)

[CHtmlEditCtrlBase](../../mfc/reference/chtmleditctrlbase-class.md)

[CHtmlView](../../mfc/reference/chtmlview-class.md)

`CHtmlEditView`

## <a name="requirements"></a>Требования

**Заголовок:** afxhtml.h

## <a name="chtmleditviewchtmleditview"></a><a name="chtmleditview"></a> CHtmlEditView:: CHtmlEditView

Формирует объект `CHtmlEditView`.

```
CHtmlEditView();
```

## <a name="chtmleditviewcreate"></a><a name="create"></a> CHtmlEditView:: Create

Создает новый объект Window.

```
virtual BOOL Create(
    LPCTSTR lpszClassName,
    LPCTSTR lpszWindowName,
    DWORD dwStyle,
    const RECT& rect,
    CWnd* pParentWnd,
    UINT nID,
    CCreateContext* pContext = NULL);
```

### <a name="parameters"></a>Параметры

*лпсзкласснаме*<br/>
Указывает на строку символов, завершающуюся нулем, которая именует класс Windows. Именем класса может быть любое имя, зарегистрированное с помощью глобальной функции [афксрегистервндкласс](application-information-and-management.md#afxregisterwndclass) или `RegisterClass` функции Windows. Если значение равно NULL, использует стандартные атрибуты [CFrameWnd](../../mfc/reference/cframewnd-class.md) по умолчанию.

*лпсзвиндовнаме*<br/>
Указывает на строку символов, завершающуюся нулем, которая представляет имя окна.

*двстиле*<br/>
Задает атрибуты стиля окна. По умолчанию устанавливаются стили WS_VISIBLE и WS_CHILD Windows.

*rect*<br/>
Ссылка на структуру [Rect](/windows/win32/api/windef/ns-windef-rect) , указывающую размер и расположение окна. Значение *ректдефаулт* позволяет Windows указать размер и расположение нового окна.

*ппарентвнд*<br/>
Указатель на родительское окно элемента управления.

*nID*<br/>
ИДЕНТИФИКАЦИОНный номер представления. По умолчанию задайте для значение AFX_IDW_PANE_FIRST.

*pContext*<br/>
Указатель на [ккреатеконтекст](../../mfc/reference/ccreatecontext-structure.md). По умолчанию имеет значение NULL.

### <a name="remarks"></a>Комментарии

Этот метод также вызывает метод автономного WebBrowser `Navigate` для загрузки документа по умолчанию (см. [CHtmlEditView:: жетстартдокумент](#getstartdocument)).

## <a name="chtmleditviewgetdhtmldocument"></a><a name="getdhtmldocument"></a> CHtmlEditView:: Жетдхтмлдокумент

Возвращает `IHTMLDocument2` интерфейс текущего документа.

```
BOOL GetDHtmlDocument(IHTMLDocument2** ppDocument) const;
```

### <a name="parameters"></a>Параметры

*ппдокумент*<br/>
Интерфейс [IHTMLDocument2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752574\(v=vs.85\)) .

## <a name="chtmleditviewgetstartdocument"></a><a name="getstartdocument"></a> CHtmlEditView:: Жетстартдокумент

Возвращает имя документа по умолчанию для этого представления.

```
virtual LPCTSTR GetStartDocument();
```

## <a name="see-also"></a>См. также раздел

[Пример Хтмледит](../../overview/visual-cpp-samples.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
