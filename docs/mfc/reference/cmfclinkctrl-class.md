---
description: 'Дополнительные сведения о: Кмфклинкктрл Class'
title: Класс Кмфклинкктрл
ms.date: 11/04/2016
f1_keywords:
- CMFCLinkCtrl
- AFXLINKCTRL/CMFCLinkCtrl
- AFXLINKCTRL/CMFCLinkCtrl::SetURL
- AFXLINKCTRL/CMFCLinkCtrl::SetURLPrefix
- AFXLINKCTRL/CMFCLinkCtrl::SizeToContent
- AFXLINKCTRL/CMFCLinkCtrl::OnDrawFocusRect
helpviewer_keywords:
- CMFCLinkCtrl [MFC], SetURL
- CMFCLinkCtrl [MFC], SetURLPrefix
- CMFCLinkCtrl [MFC], SizeToContent
- CMFCLinkCtrl [MFC], OnDrawFocusRect
ms.assetid: 80f3874d-7cc8-410e-9ff1-62a225f5034b
ms.openlocfilehash: 6951f086ac99c4b8a8260a79ee08d54476694350
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97265224"
---
# <a name="cmfclinkctrl-class"></a>Класс Кмфклинкктрл

`CMFCLinkCtrl`Класс отображает кнопку в виде гиперссылки и вызывает цель ссылки при нажатии кнопки.

## <a name="syntax"></a>Синтаксис

```
class CMFCLinkCtrl : public CMFCButton
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфклинкктрл:: SetURL](#seturl)|Отображает указанный URL-адрес в качестве текста кнопки.|
|[Кмфклинкктрл:: Сетурлпрефикс](#seturlprefix)|Задает неявный протокол (например, "http:") URL-адреса.|
|[Кмфклинкктрл:: SizeToContent](#sizetocontent)|Изменяет размер кнопки, чтобы она содержала текст или точечный рисунок кнопки.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кмфклинкктрл:: Ондравфокусрект](#ondrawfocusrect)|Вызывается структурой перед прорисовкой прямоугольника фокуса кнопки.|

## <a name="remarks"></a>Комментарии

При нажатии кнопки, производной от `CMFCLinkCtrl` класса, платформа передает URL-адрес кнопки в качестве параметра в `ShellExecute` метод. Затем `ShellExecute` метод открывает целевой объект URL-адреса.

## <a name="example"></a>Пример

В следующем примере показано, как задать размер `CMFCLinkCtrl` объекта, а также задать URL-адрес и подсказку в `CMFCLinkCtrl` объекте. Этот пример является частью [примера новых элементов управления](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_NewControls#9](../../mfc/reference/codesnippet/cpp/cmfclinkctrl-class_1.h)]
[!code-cpp[NVC_MFC_NewControls#10](../../mfc/reference/codesnippet/cpp/cmfclinkctrl-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CButton](../../mfc/reference/cbutton-class.md)

[CMFCButton](../../mfc/reference/cmfcbutton-class.md)

[CMFCLinkCtrl](../../mfc/reference/cmfclinkctrl-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкслинкктрл. h

## <a name="cmfclinkctrlondrawfocusrect"></a><a name="ondrawfocusrect"></a> Кмфклинкктрл:: Ондравфокусрект

Вызывается структурой перед прорисовкой прямоугольника фокуса кнопки.

```
virtual void OnDrawFocusRect(
    CDC* pDC,
    const CRect& rectClient);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*ректклиент*<br/>
окне Прямоугольник, ограничивающий элемент управления Link.

### <a name="remarks"></a>Комментарии

Переопределите этот метод, если вы хотите использовать собственный код для рисования прямоугольника фокуса кнопки.

## <a name="cmfclinkctrlseturl"></a><a name="seturl"></a> Кмфклинкктрл:: SetURL

Отображает указанный URL-адрес в качестве текста кнопки.

```cpp
void SetURL(LPCTSTR lpszURL);
```

### <a name="parameters"></a>Параметры

*лпсзурл*<br/>
окне Отображаемый текст кнопки.

### <a name="remarks"></a>Комментарии

## <a name="cmfclinkctrlseturlprefix"></a><a name="seturlprefix"></a> Кмфклинкктрл:: Сетурлпрефикс

Задает неявный протокол (например, "http:") URL-адреса.

```cpp
void SetURLPrefix(LPCTSTR lpszPrefix);
```

### <a name="parameters"></a>Параметры

*лпсзпрефикс*<br/>
окне Префикс протокола URL-адреса.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы задать префикс URL-адреса. Префикс не отображается на лицевой кнопке, но его можно использовать для перехода к цели URL-адреса.

## <a name="cmfclinkctrlsizetocontent"></a><a name="sizetocontent"></a> Кмфклинкктрл:: SizeToContent

Изменяет размер кнопки, чтобы она содержала текст или точечный рисунок кнопки.

```
virtual CSize SizeToContent(
    BOOL bVCenter=FALSE,
    BOOL bHCenter=FALSE);
```

### <a name="parameters"></a>Параметры

*бвцентер*<br/>
окне Значение TRUE, чтобы центрировать текст кнопки и точечный рисунок вертикально между верхней и нижней границей элемента управления "ссылка". в противном случае — значение FALSE. Значение по умолчанию — FALSE.

*бхцентер*<br/>
окне Значение TRUE, чтобы центрировать текст кнопки и точечный рисунок горизонтально между левым и правым краями элемента управления "ссылка". в противном случае — значение FALSE. Значение по умолчанию — FALSE.

### <a name="return-value"></a>Возвращаемое значение

Объект [ксизе](../../atl-mfc-shared/reference/csize-class.md) , содержащий новый размер элемента управления ссылки.

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CLinkCtrl](../../mfc/reference/clinkctrl-class.md)<br/>
[Класс Кмфкбуттон](../../mfc/reference/cmfcbutton-class.md)
