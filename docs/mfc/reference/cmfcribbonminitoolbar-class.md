---
description: 'Дополнительные сведения о: Кмфкриббонминитулбар Class'
title: Класс Кмфкриббонминитулбар
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonMiniToolBar
- AFXRIBBONMINITOOLBAR/CMFCRibbonMiniToolBar
- AFXRIBBONMINITOOLBAR/CMFCRibbonMiniToolBar::IsContextMenuMode
- AFXRIBBONMINITOOLBAR/CMFCRibbonMiniToolBar::IsRibbonMiniToolBar
- AFXRIBBONMINITOOLBAR/CMFCRibbonMiniToolBar::SetCommands
- AFXRIBBONMINITOOLBAR/CMFCRibbonMiniToolBar::Show
- AFXRIBBONMINITOOLBAR/CMFCRibbonMiniToolBar::ShowWithContextMenu
helpviewer_keywords:
- CMFCRibbonMiniToolBar [MFC], IsContextMenuMode
- CMFCRibbonMiniToolBar [MFC], IsRibbonMiniToolBar
- CMFCRibbonMiniToolBar [MFC], SetCommands
- CMFCRibbonMiniToolBar [MFC], Show
- CMFCRibbonMiniToolBar [MFC], ShowWithContextMenu
ms.assetid: 7017e963-aeaf-4fe9-b540-e15a7ed41e94
ms.openlocfilehash: 7215349323f8039bccb24860e4e5ad663bd24bcd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97273947"
---
# <a name="cmfcribbonminitoolbar-class"></a>Класс Кмфкриббонминитулбар

Реализует контекстно-зависимую панель инструментов контекстного меню.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonMiniToolBar : public CMFCRibbonPanelMenu
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCRibbonMiniToolBar::CMFCRibbonMiniToolBar`|Конструктор по умолчанию.|
|`CMFCRibbonMiniToolBar::~CMFCRibbonMiniToolBar`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|`CMFCRibbonMiniToolBar::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|`CMFCRibbonMiniToolBar::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|
|[CMFCRibbonMiniToolBar::IsContextMenuMode](#iscontextmenumode)||
|[CMFCRibbonMiniToolBar::IsRibbonMiniToolBar](#isribbonminitoolbar)|(Переопределяет `CMFCPopupMenu::IsRibbonMiniToolBar`.)|
|[CMFCRibbonMiniToolBar::SetCommands](#setcommands)|Задает список команд, отображаемых на панели инструментов.|
|[CMFCRibbonMiniToolBar::Show](#show)|Отображает мини-панель инструментов по указанным координатам экрана.|
|[CMFCRibbonMiniToolBar::ShowWithContextMenu](#showwithcontextmenu)|Отображает мини-панель инструментов вместе с контекстным меню.|

## <a name="remarks"></a>Комментарии

Мини-панель инструментов обычно отображается, когда пользователь выделяет объект в документе. Например, после выделения блока текста в текстовом редакторе отображается мини-панель инструментов с командами форматирования текста.

Когда указатель мыши выходит за пределы мини-панели инструментов, она становится прозрачной.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CFrameWnd](../../mfc/reference/cframewnd-class.md)

[CMiniFrameWnd](../../mfc/reference/cminiframewnd-class.md)

[CMFCPopupMenu](../../mfc/reference/cmfcpopupmenu-class.md)

`CMFCRibbonPanelMenu`

[CMFCRibbonMiniToolBar](../../mfc/reference/cmfcribbonminitoolbar-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонминитулбар. h

## <a name="cmfcribbonminitoolbarsetcommands"></a><a name="setcommands"></a> Кмфкриббонминитулбар:: Сеткоммандс

Задает список команд, отображаемых на панели инструментов.

```cpp
void SetCommands(
    CMFCRibbonBar* pRibbonBar,
    const CList<UINT,UINT>& lstCommands);
```

### <a name="parameters"></a>Параметры

*приббонбар*<br/>
окне Панель ленты, на которой мини-панель инструментов ищет кнопки для показа.

*лсткоммандс*<br/>
окне Список команд, отображаемых на мини-панели инструментов. Поиск связанных кнопок осуществляется по всем категориям ленты.

### <a name="remarks"></a>Комментарии

Эта функция используется для задания списка команд, отображаемых на мини-панели инструментов.

### <a name="example"></a>Пример

В следующем примере показано, как использовать `SetCommands` метод `CMFCRibbonMiniToolBar` класса. Этот фрагмент кода является частью [демонстрационного примера MS Office 2007](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_MSOffice2007Demo#9](../../mfc/reference/codesnippet/cpp/cmfcribbonminitoolbar-class_1.cpp)]

## <a name="cmfcribbonminitoolbarshow"></a><a name="show"></a> Кмфкриббонминитулбар:: показывать

Отображает мини-панель инструментов по указанным координатам экрана.

```
BOOL Show(
    int x,
    int y);
```

### <a name="parameters"></a>Параметры

*x*<br/>
окне Задает горизонтальное расположение мини-панели инструментов в экранных координатах.

*y*<br/>
окне Задает вертикальное расположение мини-панели инструментов в экранных координатах.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если мини-панель инструментов отображалась успешно; в противном случае — значение FALSE.

## <a name="cmfcribbonminitoolbarshowwithcontextmenu"></a><a name="showwithcontextmenu"></a> Кмфкриббонминитулбар:: Шоввисконтекстмену

Отображает мини-панель инструментов вместе с контекстным меню.

```
BOOL ShowWithContextMenu(
    int x,
    int y,
    UINT uiMenuResID,
    CWnd* pWndOwner);
```

### <a name="parameters"></a>Параметры

*x*<br/>
окне Задает горизонтальное расположение контекстного меню в экранных координатах.

*y*<br/>
окне Задает вертикальное расположение контекстного меню в экранных координатах.

*уименуресид*<br/>
окне Указывает идентификатор ресурса отображаемого контекстного меню.

*пвндовнер*<br/>
окне Определяет окно, которое получает сообщения из контекстного меню.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если контекстное меню было успешно отображено. в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Эта функция используется для вывода мини-панели инструментов с контекстным меню. Контекстное меню располагается на 15 пикселей под мини-панелью инструментов.

## <a name="cmfcribbonminitoolbariscontextmenumode"></a><a name="iscontextmenumode"></a> Кмфкриббонминитулбар:: Исконтекстменумоде

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
BOOL IsContextMenuMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonminitoolbarisribbonminitoolbar"></a><a name="isribbonminitoolbar"></a> Кмфкриббонминитулбар:: Исриббонминитулбар

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual BOOL IsRibbonMiniToolBar() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)
