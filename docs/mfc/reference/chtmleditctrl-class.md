---
description: 'Дополнительные сведения о: Чтмледитктрл Class'
title: Класс Чтмледитктрл
ms.date: 11/04/2016
f1_keywords:
- CHtmlEditCtrl
- AFXHTML/CHtmlEditCtrl
- AFXHTML/CHtmlEditCtrl::CHtmlEditCtrl
- AFXHTML/CHtmlEditCtrl::Create
- AFXHTML/CHtmlEditCtrl::GetDHtmlDocument
- AFXHTML/CHtmlEditCtrl::GetStartDocument
helpviewer_keywords:
- CHtmlEditCtrl [MFC], CHtmlEditCtrl
- CHtmlEditCtrl [MFC], Create
- CHtmlEditCtrl [MFC], GetDHtmlDocument
- CHtmlEditCtrl [MFC], GetStartDocument
ms.assetid: 0fc4a238-b05f-4874-9edc-6a6701f064d9
ms.openlocfilehash: d395f0f9f3e8b5ae10ad0ce35b2b1e410633e8d4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97184001"
---
# <a name="chtmleditctrl-class"></a>Класс Чтмледитктрл

Предоставляет функциональные возможности элемента управления ActiveX WebBrowser в окне MFC.

## <a name="syntax"></a>Синтаксис

```
class CHtmlEditCtrl: public CWnd,
    public CHtmlEditCtrlBase<CHtmlEditCtrl>
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Чтмледитктрл:: Чтмледитктрл](#chtmleditctrl)|Формирует объект `CHtmlEditCtrl`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Чтмледитктрл:: Create](#create)|Создает элемент управления ActiveX WebBrowser и прикрепляет его к `CHtmlEditCtrl` объекту. Эта функция автоматически помещает элемент управления WebBrowser ActiveX в режим редактирования.|
|[Чтмледитктрл:: Жетдхтмлдокумент](#getdhtmldocument)|Извлекает интерфейс [IHTMLDocument2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752574\(v=vs.85\)) для документа, загруженного в данный момент в элемент управления WebBrowser.|
|[Чтмледитктрл:: Жетстартдокумент](#getstartdocument)|Извлекает URL-адрес документа по умолчанию для загрузки в элемент управления WebBrowser.|

## <a name="remarks"></a>Комментарии

Размещенный элемент управления WebBrowser автоматически переходит в режим редактирования после его создания.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CHtmlEditCtrlBase](../../mfc/reference/chtmleditctrlbase-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

`CHtmlEditCtrl`

## <a name="requirements"></a>Требования

**Заголовок:** afxhtml.h

## <a name="chtmleditctrlchtmleditctrl"></a><a name="chtmleditctrl"></a> Чтмледитктрл:: Чтмледитктрл

Формирует объект `CHtmlEditCtrl`.

```
CHtmlEditCtrl();
```

## <a name="chtmleditctrlcreate"></a><a name="create"></a> Чтмледитктрл:: Create

Создает элемент управления ActiveX WebBrowser и прикрепляет его к `CHtmlEditCtrl` объекту. Элемент управления ActiveX WebBrowser автоматически переходит к документу по умолчанию, а затем помещается в режим редактирования этой функцией.

```
virtual BOOL Create(
    LPCTSTR lpszWindowName,
    DWORD dwStyle,
    const RECT& rect,
    CWnd* pParentWnd,
    int nID,
    CCreateContext* pContext = NULL);
```

### <a name="parameters"></a>Параметры

*лпсзвиндовнаме*<br/>
Этот параметр не используется.

*двстиле*<br/>
Этот параметр не используется.

*rect*<br/>
Задает размер и расположение элемента управления.

*ппарентвнд*<br/>
Указывает родительское окно элемента управления. Оно не должно иметь значение NULL.

*nID*<br/>
Указывает идентификатор элемента управления.

*pContext*<br/>
Этот параметр не используется.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

## <a name="chtmleditctrlgetdhtmldocument"></a><a name="getdhtmldocument"></a> Чтмледитктрл:: Жетдхтмлдокумент

Получает интерфейс [IHTMLDocument2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752574\(v=vs.85\)) для документа, загруженного в данный момент в элемент управления WebBrowser

```
BOOL GetDHtmlDocument(IHTMLDocument2** ppDocument) const;
```

### <a name="parameters"></a>Параметры

*ппдокумент*<br/>
Интерфейс документа.

## <a name="chtmleditctrlgetstartdocument"></a><a name="getstartdocument"></a> Чтмледитктрл:: Жетстартдокумент

Извлекает URL-адрес документа по умолчанию для загрузки в элемент управления WebBrowser.

```
virtual LPCTSTR GetStartDocument();
```

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
