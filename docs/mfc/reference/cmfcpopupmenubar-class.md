---
description: 'Дополнительные сведения о: CMFCPopupMenuBar Class'
title: Класс CMFCPopupMenuBar
ms.date: 11/04/2016
f1_keywords:
- CMFCPopupMenuBar
- AFXPOPUPMENUBAR/CMFCPopupMenuBar
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::AdjustSizeImmediate
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::BuildOrigItems
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::CloseDelayedSubMenu
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::ExportToMenu
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::FindDestintationToolBar
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::GetCurrentMenuImageSize
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::GetDefaultMenuId
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::GetLastCommandIndex
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::GetOffset
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::ImportFromMenu
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::IsDropDownListMode
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::IsPaletteMode
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::IsRibbonPanel
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::IsRibbonPanelInRegularMode
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::LoadFromHash
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::RestoreDelayedSubMenu
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::SetButtonStyle
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::SetOffset
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::StartPopupMenuTimer
- AFXPOPUPMENUBAR/CMFCPopupMenuBar::m_bDisableSideBarInXPMode
helpviewer_keywords:
- CMFCPopupMenuBar [MFC], AdjustSizeImmediate
- CMFCPopupMenuBar [MFC], BuildOrigItems
- CMFCPopupMenuBar [MFC], CloseDelayedSubMenu
- CMFCPopupMenuBar [MFC], ExportToMenu
- CMFCPopupMenuBar [MFC], FindDestintationToolBar
- CMFCPopupMenuBar [MFC], GetCurrentMenuImageSize
- CMFCPopupMenuBar [MFC], GetDefaultMenuId
- CMFCPopupMenuBar [MFC], GetLastCommandIndex
- CMFCPopupMenuBar [MFC], GetOffset
- CMFCPopupMenuBar [MFC], ImportFromMenu
- CMFCPopupMenuBar [MFC], IsDropDownListMode
- CMFCPopupMenuBar [MFC], IsPaletteMode
- CMFCPopupMenuBar [MFC], IsRibbonPanel
- CMFCPopupMenuBar [MFC], IsRibbonPanelInRegularMode
- CMFCPopupMenuBar [MFC], LoadFromHash
- CMFCPopupMenuBar [MFC], RestoreDelayedSubMenu
- CMFCPopupMenuBar [MFC], SetButtonStyle
- CMFCPopupMenuBar [MFC], SetOffset
- CMFCPopupMenuBar [MFC], StartPopupMenuTimer
- CMFCPopupMenuBar [MFC], m_bDisableSideBarInXPMode
ms.assetid: 4c93c459-7f70-4240-8c63-280bb811e374
ms.openlocfilehash: 4db8c02ed92aec5243f9a2c7800c6fd1f9747751
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334746"
---
# <a name="cmfcpopupmenubar-class"></a>Класс CMFCPopupMenuBar

Строка меню, внедренная в контекстное меню.

## <a name="syntax"></a>Синтаксис

```
class CMFCPopupMenuBar : public CMFCToolBar
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCPopupMenuBar::AdjustSizeImmediate](#adjustsizeimmediate)|Немедленное повторное вычисление макета панели. (Переопределяет [CPane:: аджустсизеиммедиате](../../mfc/reference/cpane-class.md#adjustsizeimmediate).)|
|[CMFCPopupMenuBar::BuildOrigItems](#buildorigitems)|Загружает элементы всплывающего меню из указанного ресурса меню.|
|[CMFCPopupMenuBar::CloseDelayedSubMenu](#closedelayedsubmenu)|Закрывает кнопку отложенного всплывающего меню.|
|[CMFCPopupMenuBar::ExportToMenu](#exporttomenu)|Создает меню на основе кнопок всплывающего меню.|
|[CMFCPopupMenuBar::FindDestintationToolBar](#finddestintationtoolbar)|Находит панель инструментов, где находится указанная точка.|
|[CMFCPopupMenuBar::GetCurrentMenuImageSize](#getcurrentmenuimagesize)|Указывает размер изображений на кнопке меню.|
|[CMFCPopupMenuBar::GetDefaultMenuId](#getdefaultmenuid)|Возвращает идентификатор элемента меню по умолчанию.|
|[CMFCPopupMenuBar::GetLastCommandIndex](#getlastcommandindex)|Возвращает индекс последней вызванной команды меню.|
|[CMFCPopupMenuBar::GetOffset](#getoffset)|Возвращает смещение строки всплывающего меню.|
|[CMFCPopupMenuBar::ImportFromMenu](#importfrommenu)|Импортирует кнопки всплывающего меню из указанного меню.|
|[CMFCPopupMenuBar::IsDropDownListMode](#isdropdownlistmode)|Указывает, находится ли всплывающее меню в режиме раскрывающегося списка.|
|[CMFCPopupMenuBar::IsPaletteMode](#ispalettemode)|Указывает, находится ли всплывающее меню в режиме палитры.|
|[CMFCPopupMenuBar::IsRibbonPanel](#isribbonpanel)|Указывает, является ли это панелью ленты (по умолчанию FALSE).|
|[CMFCPopupMenuBar::IsRibbonPanelInRegularMode](#isribbonpanelinregularmode)|Указывает, является ли эта панелью ленты в обычном режиме (по умолчанию FALSE).|
|[CMFCPopupMenuBar::LoadFromHash](#loadfromhash)|Загружает заархивированное меню.|
|[CMFCPopupMenuBar::RestoreDelayedSubMenu](#restoredelayedsubmenu)|Восстанавливает отложенную кнопку меню для закрытия всплывающей панели меню.|
|[CMFCPopupMenuBar::SetButtonStyle](#setbuttonstyle)|Задает стиль кнопки панели инструментов с заданным индексом. (Переопределяет [CMFCToolBar:: сетбуттонстиле](../../mfc/reference/cmfctoolbar-class.md#setbuttonstyle).)|
|[CMFCPopupMenuBar::SetOffset](#setoffset)|Задает смещение строки всплывающего меню.|
|[CMFCPopupMenuBar::StartPopupMenuTimer](#startpopupmenutimer)|Запускает таймер для указанной кнопки задержки всплывающего меню.|

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[CMFCPopupMenuBar:: m_bDisableSideBarInXPMode](#m_bdisablesidebarinxpmode)|Указывает, будет ли отображаться серая боковая панель, если приложение имеет внешний вид Windows XP.|

## <a name="remarks"></a>Комментарии

Объект `CMFCPopupMenuBar` создается в то же время, что и [Класс CMFCPopupMenu](../../mfc/reference/cmfcpopupmenu-class.md) , и внедряется в него. `CMFCPopupMenuBar`Объект охватывает всю клиентскую область `CMFCPopupMenu` объекта. Он поддерживает ввод с клавиатуры и мыши. Он также передает эти входные данные в `CMFCPopupMenu` и в окно фрейма верхнего уровня.

## <a name="example"></a>Пример

В следующем примере показано, как инициализировать `CMFCPopupMenuBar` объект из `CMFCPopupMenu` объекта. Этот фрагмент кода входит в состав [примера Draw Client](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_DrawClient#7](../../mfc/reference/codesnippet/cpp/cmfcpopupmenubar-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[кмфкбасетулбар](../../mfc/reference/cmfcbasetoolbar-class.md)

[CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)

[CMFCPopupMenuBar](../../mfc/reference/cmfcpopupmenubar-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкспопупменубар. h

## <a name="cmfcpopupmenubaradjustsizeimmediate"></a><a name="adjustsizeimmediate"></a> CMFCPopupMenuBar:: Аджустсизеиммедиате

Немедленно пересчитывает макет панели всплывающего меню. (Переопределяет [CPane:: аджустсизеиммедиате](../../mfc/reference/cpane-class.md#adjustsizeimmediate).

```
virtual void AdjustSizeImmediate(BOOL bRecalcLayout);
```

### <a name="parameters"></a>Параметры

*bRecalcLayout*<br/>
окне Значение TRUE, чтобы автоматически пересчитать макет панели всплывающего меню; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarbuildorigitems"></a><a name="buildorigitems"></a> CMFCPopupMenuBar:: Буилдоригитемс

Загружает элементы всплывающего меню из указанного ресурса меню.

```
BOOL BuildOrigItems(UINT uiMenuResID);
```

### <a name="parameters"></a>Параметры

*уименуресид*<br/>
окне Указывает идентификатор меню загружаемого ресурса меню.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE в случае успеха или FALSE в противном случае.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarclosedelayedsubmenu"></a><a name="closedelayedsubmenu"></a> CMFCPopupMenuBar:: Клоседелайедсубмену

Закрывает кнопку всплывающего меню, которая была отложена.

```
virtual void CloseDelayedSubMenu();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarexporttomenu"></a><a name="exporttomenu"></a> CMFCPopupMenuBar:: Експорттомену

Создает меню на основе кнопок всплывающего меню.

```
virtual HMENU ExportToMenu() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает маркер в новое меню.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarfinddestintationtoolbar"></a><a name="finddestintationtoolbar"></a> CMFCPopupMenuBar:: Финддестинтатионтулбар

Находит панель инструментов, где находится указанная точка.

```
CMFCToolBar* FindDestintationToolBar(CPoint point);
```

### <a name="parameters"></a>Параметры

*точки*<br/>
окне Точка на экране.

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на панель инструментов, где находится точка, если она существует, или значение NULL, если нет.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubargetcurrentmenuimagesize"></a><a name="getcurrentmenuimagesize"></a> CMFCPopupMenuBar:: Жеткуррентменуимажесизе

Указывает размер изображений на кнопке меню.

```
virtual CSize GetCurrentMenuImageSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает размер изображений на кнопке меню на панели инструментов.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubargetdefaultmenuid"></a><a name="getdefaultmenuid"></a> CMFCPopupMenuBar:: Жетдефаултменуид

Возвращает идентификатор элемента меню по умолчанию.

```
UINT GetDefaultMenuId() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает идентификатор элемента меню по умолчанию во всплывающей строке меню.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubargetlastcommandindex"></a><a name="getlastcommandindex"></a> CMFCPopupMenuBar:: Жетласткоммандиндекс

Возвращает индекс последней вызванной команды меню.

```
static int __stdcall GetLastCommandIndex();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает индекс последней вызываемой команды меню.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubargetoffset"></a><a name="getoffset"></a> CMFCPopupMenuBar:: offset

Возвращает смещение строки всплывающего меню.

```
int GetOffset() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает смещение строки всплывающего меню.

### <a name="remarks"></a>Комментарии

Это значение задается с помощью [CMFCPopupMenuBar:: сетоффсет](#setoffset).

## <a name="cmfcpopupmenubarimportfrommenu"></a><a name="importfrommenu"></a> CMFCPopupMenuBar:: Импортфроммену

Импортирует кнопки всплывающего меню из указанного меню.

```
virtual BOOL ImportFromMenu(
    HMENU hMenu,
    BOOL bShowAllCommands = FALSE);
```

### <a name="parameters"></a>Параметры

*hMenu*<br/>
окне Меню, из которого импортируются кнопки всплывающего меню.

*бшоваллкоммандс*<br/>
окне Значение TRUE, если все команды в меню должны быть импортированы, или значение FALSE, если редко используемые шаблоны могут быть скрыты.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если кнопки меню были успешно импортированы из меню, или значение FALSE в противном случае.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarisdropdownlistmode"></a><a name="isdropdownlistmode"></a> CMFCPopupMenuBar:: Исдропдовнлистмоде

Указывает, находится ли всплывающее меню в режиме раскрывающегося списка.

```
BOOL IsDropDownListMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если всплывающая строка меню находится в режиме раскрывающегося списка, или значение FALSE в противном случае.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarispalettemode"></a><a name="ispalettemode"></a> CMFCPopupMenuBar:: Испалеттемоде

Указывает, находится ли всплывающее меню в режиме палитры.

```
BOOL IsPaletteMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если режим палитры включен, или FALSE в противном случае.

### <a name="remarks"></a>Комментарии

Если в строке меню выбран режим палитры, то пункты меню отображаются в нескольких столбцах и ограниченном количестве строк.

## <a name="cmfcpopupmenubarisribbonpanel"></a><a name="isribbonpanel"></a> CMFCPopupMenuBar:: Исриббонпанел

Указывает, является ли это панелью ленты (по умолчанию FALSE).

```
virtual BOOL IsRibbonPanel() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение FALSE по умолчанию, указывающее, что это не панель ленты.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarisribbonpanelinregularmode"></a><a name="isribbonpanelinregularmode"></a> CMFCPopupMenuBar:: Исриббонпанелинрегулармоде

Указывает, является ли эта панелью ленты в обычном режиме (по умолчанию FALSE).

```
virtual BOOL IsRibbonPanelInRegularMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение FALSE по умолчанию, указывающее, что это не панель ленты в обычном режиме.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarloadfromhash"></a><a name="loadfromhash"></a> CMFCPopupMenuBar:: Лоадфромхаш

Загружает заархивированное меню.

```
BOOL LoadFromHash(HMENU hMenu);
```

### <a name="parameters"></a>Параметры

*hMenu*<br/>
окне Описатель для заархивированного меню для загрузки.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если меню загружено успешно, или значение FALSE в противном случае.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarm_bdisablesidebarinxpmode"></a><a name="m_bdisablesidebarinxpmode"></a> CMFCPopupMenuBar:: m_bDisableSideBarInXPMode

Логический параметр, указывающий, имеет ли приложение серую боковую панель, если она имеет внешний вид Windows XP.

```
BOOL m_bDisableSideBarInXPMode;
```

### <a name="remarks"></a>Комментарии

Если для этой переменной-члена задано значение FALSE и приложение имеет внешний вид Windows XP, то платформа Рисует серую боковую панель в приложении.

Значение по умолчанию — FALSE.

## <a name="cmfcpopupmenubarrestoredelayedsubmenu"></a><a name="restoredelayedsubmenu"></a> CMFCPopupMenuBar:: Рестоределайедсубмену

Восстанавливает отложенную кнопку меню для закрытия всплывающей панели меню.

```
virtual void RestoreDelayedSubMenu();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarsetbuttonstyle"></a><a name="setbuttonstyle"></a> CMFCPopupMenuBar:: Сетбуттонстиле

Задает стиль кнопки панели инструментов с заданным индексом. (Переопределяет [CMFCToolBar:: сетбуттонстиле](../../mfc/reference/cmfctoolbar-class.md#setbuttonstyle).)

```
virtual void SetButtonStyle(
    int nIndex,
    UINT nStyle);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
окне Отсчитываемый от нуля индекс кнопки панели инструментов, стиль которой должен быть установлен.

*nStyle*<br/>
окне Стиль кнопки. Список доступных стилей кнопок панели инструментов см. в разделе [стили элементов управления панели инструментов](../../mfc/reference/toolbar-control-styles.md) .

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarsetoffset"></a><a name="setoffset"></a> CMFCPopupMenuBar:: Сетоффсет

Задает смещение строки всплывающего меню.

```cpp
void SetOffset(int iOffset);
```

### <a name="parameters"></a>Параметры

*иоффсет*<br/>
окне Число строк, которое должно быть смещено в строке всплывающего меню.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpopupmenubarstartpopupmenutimer"></a><a name="startpopupmenutimer"></a> CMFCPopupMenuBar:: Стартпопупменутимер

Запускает таймер для указанной кнопки задержки всплывающего меню.

```cpp
void StartPopupMenuTimer(
    CMFCToolBarMenuButton* pMenuButton,
    int nDelayFactor = 1);
```

### <a name="parameters"></a>Параметры

*пменубуттон*<br/>
окне Указатель на кнопку меню, для которой задается таймер задержки.

*нделайфактор*<br/>
окне Коэффициент задержки, равный по крайней мере одному, для умножения на стандартное время задержки меню (обычно от половины секунды до пяти секунд).

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкколорбар](../../mfc/reference/cmfccolorbar-class.md)<br/>
[Класс CMFCPopupMenu](../../mfc/reference/cmfcpopupmenu-class.md)
