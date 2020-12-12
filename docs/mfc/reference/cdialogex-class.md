---
description: 'Дополнительные сведения о: Кдиаложекс Class'
title: Класс Кдиаложекс
ms.date: 11/04/2016
f1_keywords:
- CDialogEx
- AFXDIALOGEX/CDialogEx
- AFXDIALOGEX/CDialogEx::CDialogEx
- AFXDIALOGEX/CDialogEx::SetBackgroundColor
- AFXDIALOGEX/CDialogEx::SetBackgroundImage
helpviewer_keywords:
- CDialogEx [MFC], CDialogEx
- CDialogEx [MFC], SetBackgroundColor
- CDialogEx [MFC], SetBackgroundImage
ms.assetid: a6ed3b1f-aef8-4b66-ac78-2160faf63c13
ms.openlocfilehash: 27ec0011935871d472734cae6f0d62b402382727
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185249"
---
# <a name="cdialogex-class"></a>Класс Кдиаложекс

Класс `CDialogEx` задает цвет фона и фоновое изображение для диалогового окна.

## <a name="syntax"></a>Синтаксис

```
class CDialogEx : public CDialog
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CDialogEx::CDialogEx](#cdialogex)|Формирует объект `CDialogEx`.|
|`CDialogEx::~CDialogEx`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CDialogEx::SetBackgroundColor](#setbackgroundcolor)|Задает цвет фона диалогового окна.|
|[CDialogEx::SetBackgroundImage](#setbackgroundimage)|Задает фоновое изображение диалогового окна.|

## <a name="remarks"></a>Комментарии

Чтобы использовать класс `CDialogEx`, сформируйте класс диалогового окна из класса `CDialogEx` вместо класса `CDialog`.

Изображения диалогового окна хранятся в файле ресурсов. Платформа автоматически удаляет все изображения, загруженные из файла ресурсов. Чтобы программно удалить текущее фоновое изображение, вызовите метод [кдиаложекс:: сетбаккграундимаже](#setbackgroundimage) или реализуйте `OnDestroy` обработчик событий. При вызове метода [кдиаложекс:: сетбаккграундимаже](#setbackgroundimage) передайте `HBITMAP` параметр в качестве маркера изображения. Объект `CDialogEx` будет распоряжаться изображением и может удалить его, если для флажка `m_bAutoDestroyBmp` установлено значение `TRUE`.

`CDialogEx`Объект может быть родителем объекта [класса CMFCPopupMenu](../../mfc/reference/cmfcpopupmenu-class.md) . Объект [класса CMFCPopupMenu](../../mfc/reference/cmfcpopupmenu-class.md) вызывает метод, `CDialogEx::SetActiveMenu` когда открывается объект [класса CMFCPopupMenu](../../mfc/reference/cmfcpopupmenu-class.md) . `CDialogEx`После этого объект обрабатывает все события меню до закрытия объекта [класса CMFCPopupMenu](../../mfc/reference/cmfcpopupmenu-class.md) .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CDialogEx](../../mfc/reference/cdialogex-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксдиаложекс. h

## <a name="cdialogexcdialogex"></a><a name="cdialogex"></a> Кдиаложекс:: Кдиаложекс

Формирует объект `CDialogEx`.

```
CDialogEx(
    UINT nIDTemplate,
    CWnd* pParent=NULL);

CDialogEx(
    LPCTSTR lpszTemplateName,
    CWnd* pParentWnd=NULL);
```

### <a name="parameters"></a>Параметры

*нидтемплате*<br/>
окне Идентификатор ресурса шаблона диалогового окна.

*лпсзтемплатенаме*<br/>
окне Имя ресурса шаблона диалогового окна.

*ппарент*<br/>
окне Указатель на родительское окно. Значение по умолчанию — NULL.

*ппарентвнд*<br/>
окне Указатель на родительское окно. Значение по умолчанию — NULL.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdialogexsetbackgroundcolor"></a><a name="setbackgroundcolor"></a> Кдиаложекс:: Сетбаккграундколор

Задает цвет фона диалогового окна.

```cpp
void SetBackgroundColor(
    COLORREF color,
    BOOL bRepaint=TRUE);
```

### <a name="parameters"></a>Параметры

*color*<br/>
окне Значение цвета RGB.

*bRepaint*<br/>
окне Значение TRUE, чтобы немедленно обновить экран; в противном случае — значение FALSE. Значение по умолчанию — TRUE.

### <a name="remarks"></a>Комментарии

## <a name="cdialogexsetbackgroundimage"></a><a name="setbackgroundimage"></a> Кдиаложекс:: Сетбаккграундимаже

Задает фоновое изображение диалогового окна.

```cpp
void SetBackgroundImage(
    HBITMAP hBitmap,
    BackgroundLocation location=BACKGR_TILE,
    BOOL bAutoDestroy=TRUE,
    BOOL bRepaint=TRUE);

BOOL SetBackgroundImage(
    UINT uiBmpResId,
    BackgroundLocation location=BACKGR_TILE,
    BOOL bRepaint=TRUE);
```

### <a name="parameters"></a>Параметры

*хбитмап*<br/>
окне Маркер фонового изображения.

*уибмпресид*<br/>
окне Идентификатор ресурса фонового изображения.

*расположение*<br/>
окне Одно из `CDialogEx::BackgroundLocation` значений, задающих расположение изображения. Допустимые значения: BACKGR_TILE, BACKGR_TOPLEFT, BACKGR_TOPRIGHT, BACKGR_BOTTOMLEFT и BACKGR_BOTTOMRIGHT. Значение по умолчанию — BACKGR_TILE.

*баутодестрой*<br/>
окне Значение TRUE для автоматического уничтожения фонового изображения; в противном случае — значение FALSE.

*bRepaint*<br/>
окне Значение TRUE, чтобы немедленно перерисовывать диалоговое окно; в противном случае — значение FALSE.

### <a name="return-value"></a>Возвращаемое значение

Во втором синтаксисе перегрузки метода — TRUE, если метод выполнен успешно; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Указанное изображение не растягивается по размеру клиентской области диалогового окна.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCPopupMenu](../../mfc/reference/cmfcpopupmenu-class.md)<br/>
[Класс Кконтекстменуманажер](../../mfc/reference/ccontextmenumanager-class.md)
