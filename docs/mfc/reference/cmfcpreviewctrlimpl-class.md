---
description: 'Дополнительные сведения о: Кмфкпревиевктрлимпл Class'
title: Класс CMFCPreviewCtrlImpl
ms.date: 11/04/2016
f1_keywords:
- CMFCPreviewCtrlImpl
- AFXWIN/CMFCPreviewCtrlImpl
- AFXWIN/CMFCPreviewCtrlImpl::CMFCPreviewCtrlImpl
- AFXWIN/CMFCPreviewCtrlImpl::Create
- AFXWIN/CMFCPreviewCtrlImpl::Destroy
- AFXWIN/CMFCPreviewCtrlImpl::Focus
- AFXWIN/CMFCPreviewCtrlImpl::GetDocument
- AFXWIN/CMFCPreviewCtrlImpl::Redraw
- AFXWIN/CMFCPreviewCtrlImpl::SetDocument
- AFXWIN/CMFCPreviewCtrlImpl::SetHost
- AFXWIN/CMFCPreviewCtrlImpl::SetPreviewVisuals
- AFXWIN/CMFCPreviewCtrlImpl::SetRect
- AFXWIN/CMFCPreviewCtrlImpl::DoPaint
- AFXWIN/CMFCPreviewCtrlImpl::m_clrBackColor
- AFXWIN/CMFCPreviewCtrlImpl::m_clrTextColor
- AFXWIN/CMFCPreviewCtrlImpl::m_font
- AFXWIN/CMFCPreviewCtrlImpl::m_pDocument
helpviewer_keywords:
- CMFCPreviewCtrlImpl [MFC], CMFCPreviewCtrlImpl
- CMFCPreviewCtrlImpl [MFC], Create
- CMFCPreviewCtrlImpl [MFC], Destroy
- CMFCPreviewCtrlImpl [MFC], Focus
- CMFCPreviewCtrlImpl [MFC], GetDocument
- CMFCPreviewCtrlImpl [MFC], Redraw
- CMFCPreviewCtrlImpl [MFC], SetDocument
- CMFCPreviewCtrlImpl [MFC], SetHost
- CMFCPreviewCtrlImpl [MFC], SetPreviewVisuals
- CMFCPreviewCtrlImpl [MFC], SetRect
- CMFCPreviewCtrlImpl [MFC], DoPaint
- CMFCPreviewCtrlImpl [MFC], m_clrBackColor
- CMFCPreviewCtrlImpl [MFC], m_clrTextColor
- CMFCPreviewCtrlImpl [MFC], m_font
- CMFCPreviewCtrlImpl [MFC], m_pDocument
ms.assetid: 06257fa0-54c9-478d-9d68-c9698c3f93ed
ms.openlocfilehash: 09e4b8e023a55110986aafccfd2646d8e7775c31
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334729"
---
# <a name="cmfcpreviewctrlimpl-class"></a>Класс CMFCPreviewCtrlImpl

Этот класс реализует окно, помещенное в главное окно, предоставляемое оболочкой для расширенного просмотра.

## <a name="syntax"></a>Синтаксис

```
class CMFCPreviewCtrlImpl : public CWnd;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкпревиевктрлимпл:: ~ Кмфкпревиевктрлимпл](#dtor)|Разструктура объекта элемента управления предварительной версии.|
|[Кмфкпревиевктрлимпл:: Кмфкпревиевктрлимпл](#cmfcpreviewctrlimpl)|Конструирует объект элемента управления предварительной версии.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкпревиевктрлимпл:: Create](#create)|Перегружен. Вызывается расширенным обработчиком просмотра для создания окна Windows.|
|[Кмфкпревиевктрлимпл::D естрой](#destroy)|Вызывается расширенным обработчиком просмотра, когда ему требуется уничтожить этот элемент управления.|
|[Кмфкпревиевктрлимпл:: Focus](#focus)|Устанавливает фокус на этот элемент управления.|
|[Кмфкпревиевктрлимпл:: a Document](#getdocument)|Возвращает документ, подключенный к этому элементу управления предварительной версии.|
|[Кмфкпревиевктрлимпл:: перерисовка](#redraw)|Указывает, что этот элемент управления должен перерисовываться.|
|[Кмфкпревиевктрлимпл:: Сетдокумент](#setdocument)|Вызывается обработчиком просмотра для создания связи между реализацией документа и элементом управления предварительного просмотра.|
|[Кмфкпревиевктрлимпл:: Сесост](#sethost)|Задает новый родительский элемент для этого элемента управления.|
|[Кмфкпревиевктрлимпл:: Сетпревиеввисуалс](#setpreviewvisuals)|Вызывается расширенным обработчиком просмотра, когда ему необходимо задать визуальные элементы расширенного просмотра содержимого.|
|[Кмфкпревиевктрлимпл:: SetRect](#setrect)|Задает новый ограничивающий прямоугольник для этого элемента управления.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кмфкпревиевктрлимпл::D Опаинт](#dopaint)|Вызывается платформой для отрисовки предварительной версии.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Кмфкпревиевктрлимпл:: m_clrBackColor](#m_clrbackcolor)|Цвет фона окна предварительного просмотра.|
|[Кмфкпревиевктрлимпл:: m_clrTextColor](#m_clrtextcolor)|Цвет текста окна предварительного просмотра.|
|[Кмфкпревиевктрлимпл:: m_font](#m_font)|Шрифт, используемый для вывода текста в окне предварительного просмотра.|
|[Кмфкпревиевктрлимпл:: m_pDocument](#m_pdocument)|Указатель на документ, содержимое которого предварительно отображается в элементе управления.|

## <a name="requirements"></a>Требования

**Заголовок:** afxwin.h

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[кмфкпревиевктрлимпл](../../mfc/reference/cmfcpreviewctrlimpl-class.md)

## <a name="cmfcpreviewctrlimplcmfcpreviewctrlimpl"></a><a name="cmfcpreviewctrlimpl"></a> Кмфкпревиевктрлимпл:: Кмфкпревиевктрлимпл

Конструирует объект элемента управления предварительной версии.

### <a name="syntax"></a>Синтаксис

Кмфкпревиевктрлимпл ();

## <a name="cmfcpreviewctrlimplcreate"></a><a name="create"></a> Кмфкпревиевктрлимпл:: Create

Перегружен. Вызывается расширенным обработчиком просмотра для создания окна Windows.

### <a name="syntax"></a>Синтаксис

```
virtual BOOL Create(
   HWND hWndParent,
   const RECT* prc
);
virtual BOOL Create(
   HWND hWndParent,
   const RECT* prc,
   CCreateContext* pContext
);
```

### <a name="parameters"></a>Параметры

*хвндпарент*<br/>
Маркер главного окна, предоставляемый оболочкой для расширенной предварительной версии.

*PRC*<br/>
Задает начальный размер и расположение окна.

*pContext*<br/>
Указатель на контекст создания.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если создание прошло успешно; в противном случае — значение FALSE.

## <a name="cmfcpreviewctrlimpldestroy"></a><a name="destroy"></a> Кмфкпревиевктрлимпл::D естрой

Вызывается расширенным обработчиком просмотра, когда ему требуется уничтожить этот элемент управления.

### <a name="syntax"></a>Синтаксис

```
virtual void Destroy();
```

## <a name="cmfcpreviewctrlimpldopaint"></a><a name="dopaint"></a> Кмфкпревиевктрлимпл::D Опаинт

Вызывается платформой для отрисовки предварительной версии.

### <a name="syntax"></a>Синтаксис

```
virtual void DoPaint(
   CPaintDC* pDC
);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
Указатель на контекст устройства для рисования.

## <a name="cmfcpreviewctrlimplfocus"></a><a name="focus"></a> Кмфкпревиевктрлимпл:: Focus

Устанавливает фокус на этот элемент управления.

### <a name="syntax"></a>Синтаксис

```
virtual void Focus();
```

## <a name="cmfcpreviewctrlimplgetdocument"></a><a name="getdocument"></a> Кмфкпревиевктрлимпл:: a Document

Возвращает документ, подключенный к этому элементу управления предварительной версии.

### <a name="syntax"></a>Синтаксис

```
ATL::IDocument* GetDocument();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на документ, содержимое которого предварительно отображается в элементе управления.

## <a name="cmfcpreviewctrlimplm_clrbackcolor"></a><a name="m_clrbackcolor"></a> Кмфкпревиевктрлимпл:: m_clrBackColor

Цвет фона окна предварительного просмотра.

### <a name="syntax"></a>Синтаксис

```
COLORREF m_clrBackColor;
```

## <a name="cmfcpreviewctrlimplm_clrtextcolor"></a><a name="m_clrtextcolor"></a> Кмфкпревиевктрлимпл:: m_clrTextColor

Цвет текста окна предварительного просмотра.

### <a name="syntax"></a>Синтаксис

```
COLORREF m_clrTextColor;
```

## <a name="cmfcpreviewctrlimplm_font--font-used-to-display-text-in-the-preview-window"></a><a name="m_font"></a> Кмфкпревиевктрлимпл:: m_font шрифт, используемый для показа текста в окне предварительного просмотра.

### <a name="syntax"></a>Синтаксис

```
CFont m_font;
```

## <a name="cmfcpreviewctrlimplm_pdocument"></a><a name="m_pdocument"></a> Кмфкпревиевктрлимпл:: m_pDocument

Указатель на документ, содержимое которого предварительно отображается в элементе управления.

### <a name="syntax"></a>Синтаксис

```
ATL::IDocument* m_pDocument;
```

## <a name="cmfcpreviewctrlimplredraw"></a><a name="redraw"></a> Кмфкпревиевктрлимпл:: перерисовка

Указывает, что этот элемент управления должен перерисовываться.

### <a name="syntax"></a>Синтаксис

```
virtual void Redraw();
```

## <a name="cmfcpreviewctrlimplsetdocument"></a><a name="setdocument"></a> Кмфкпревиевктрлимпл:: Сетдокумент

Вызывается обработчиком просмотра для создания связи между реализацией документа и элементом управления предварительного просмотра.

### <a name="syntax"></a>Синтаксис

```cpp
void SetDocument(
   IDocument* pDocument
);
```

### <a name="parameters"></a>Параметры

*пдокумент*<br/>
Указатель на реализацию документа.

## <a name="cmfcpreviewctrlimplsethost"></a><a name="sethost"></a> Кмфкпревиевктрлимпл:: Сесост

Задает новый родительский элемент для этого элемента управления.

### <a name="syntax"></a>Синтаксис

```
virtual void SetHost(
   HWND hWndParent
);
```

### <a name="parameters"></a>Параметры

*хвндпарент*<br/>
Дескриптор нового родительского окна.

## <a name="cmfcpreviewctrlimplsetpreviewvisuals"></a><a name="setpreviewvisuals"></a> Кмфкпревиевктрлимпл:: Сетпревиеввисуалс

Вызывается расширенным обработчиком просмотра, когда ему необходимо задать визуальные элементы расширенного просмотра содержимого.

### <a name="syntax"></a>Синтаксис

```
virtual void SetPreviewVisuals(
   COLORREF clrBack,
   COLORREF clrText,
   const LOGFONTW *plf
);
```

### <a name="parameters"></a>Параметры

*клрбакк*<br/>
Цвет фона окна предварительного просмотра.

*clrText*<br/>
Цвет текста окна предварительного просмотра.

*плф*<br/>
Шрифт, используемый для вывода текста в окне предварительного просмотра.

## <a name="cmfcpreviewctrlimplsetrect"></a><a name="setrect"></a> Кмфкпревиевктрлимпл:: SetRect

Задает новый ограничивающий прямоугольник для этого элемента управления.

### <a name="syntax"></a>Синтаксис

```
virtual void SetRect(
   const RECT* prc,
   BOOL bRedraw
);
```

### <a name="parameters"></a>Параметры

*PRC*<br/>
Указывает новый размер и расположение элемента управления предварительной версии.

*bRedraw*<br/>
Указывает, следует ли перерисовать элемент управления.

### <a name="remarks"></a>Комментарии

Обычно при изменении размера элемента управления ведущего приложения задается новый ограничивающий прямоугольник.

## <a name="cmfcpreviewctrlimplcmfcpreviewctrlimpl"></a><a name="dtor"></a> Кмфкпревиевктрлимпл:: ~ Кмфкпревиевктрлимпл

Разструктура объекта элемента управления предварительной версии.

### <a name="syntax"></a>Синтаксис

```
virtual ~CMFCPreviewCtrlImpl();
```
