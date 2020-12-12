---
description: 'Дополнительные сведения о: CMFCOutlookBar Class'
title: Класс CMFCOutlookBar
ms.date: 06/25/2018
f1_keywords:
- CMFCOutlookBar
- AFXOUTLOOKBAR/CMFCOutlookBar
- AFXOUTLOOKBAR/CMFCOutlookBar::AllowDestroyEmptyTabbedPane
- AFXOUTLOOKBAR/CMFCOutlookBar::CanAcceptPane
- AFXOUTLOOKBAR/CMFCOutlookBar::CanSetCaptionTextToTabName
- AFXOUTLOOKBAR/CMFCOutlookBar::Create
- AFXOUTLOOKBAR/CMFCOutlookBar::CreateCustomPage
- AFXOUTLOOKBAR/CMFCOutlookBar::DoesAllowDynInsertBefore
- AFXOUTLOOKBAR/CMFCOutlookBar::FloatTab
- AFXOUTLOOKBAR/CMFCOutlookBar::GetButtonsFont
- AFXOUTLOOKBAR/CMFCOutlookBar::GetTabArea
- AFXOUTLOOKBAR/CMFCOutlookBar::IsMode2003
- AFXOUTLOOKBAR/CMFCOutlookBar::OnAfterAnimation
- AFXOUTLOOKBAR/CMFCOutlookBar::OnBeforeAnimation
- AFXOUTLOOKBAR/CMFCOutlookBar::OnScroll
- AFXOUTLOOKBAR/CMFCOutlookBar::RemoveCustomPage
- AFXOUTLOOKBAR/CMFCOutlookBar::SetButtonsFont
- AFXOUTLOOKBAR/CMFCOutlookBar::SetMode2003
helpviewer_keywords:
- CMFCOutlookBar [MFC], AllowDestroyEmptyTabbedPane
- CMFCOutlookBar [MFC], CanAcceptPane
- CMFCOutlookBar [MFC], CanSetCaptionTextToTabName
- CMFCOutlookBar [MFC], Create
- CMFCOutlookBar [MFC], CreateCustomPage
- CMFCOutlookBar [MFC], DoesAllowDynInsertBefore
- CMFCOutlookBar [MFC], FloatTab
- CMFCOutlookBar [MFC], GetButtonsFont
- CMFCOutlookBar [MFC], GetTabArea
- CMFCOutlookBar [MFC], IsMode2003
- CMFCOutlookBar [MFC], OnAfterAnimation
- CMFCOutlookBar [MFC], OnBeforeAnimation
- CMFCOutlookBar [MFC], OnScroll
- CMFCOutlookBar [MFC], RemoveCustomPage
- CMFCOutlookBar [MFC], SetButtonsFont
- CMFCOutlookBar [MFC], SetMode2003
ms.assetid: 2b335f71-ce99-4efd-b103-e65ba43ffc36
ms.openlocfilehash: e54e44e702aaf8d6883ada6be9c127f63ecee97d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97265042"
---
# <a name="cmfcoutlookbar-class"></a>Класс CMFCOutlookBar

Область со вкладками, которая имеет внешний вид области **Область переходов** в Microsoft Outlook 2000 или Outlook 2003. `CMFCOutlookBar`Объект содержит объект [класса кмфкаутлукбартабктрл](../../mfc/reference/cmfcoutlookbartabctrl-class.md) и ряд вкладок. Вкладки могут быть либо [CMFCOutlookBarPane объектами класса](../../mfc/reference/cmfcoutlookbarpane-class.md) , либо `CWnd` производными объектами. Пользователю панель Outlook отображается как последовательность кнопок и область отображения. Когда пользователь нажимает кнопку, отображается соответствующая область элемента управления или кнопки.

## <a name="syntax"></a>Синтаксис

```cpp
class CMFCOutlookBar : public CBaseTabbedPane
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCOutlookBar::CMFCOutlookBar`|Конструктор по умолчанию.|
|`CMFCOutlookBar::~CMFCOutlookBar`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCOutlookBar::AllowDestroyEmptyTabbedPane](#allowdestroyemptytabbedpane)|Указывает, можно ли уничтожить пустую панель с вкладками. (Переопределяет [CBaseTabbedPane:: алловдестройемптитаббедпане](../../mfc/reference/cbasetabbedpane-class.md#allowdestroyemptytabbedpane).)|
|[CMFCOutlookBar:: Канакцептпане](#canacceptpane)|Определяет, можно ли прикрепить другую панель к панели Outlook. (Переопределяет CDockablePane:: Канакцептпане.)|
|[CMFCOutlookBar:: Кансеткаптионтексттотабнаме](#cansetcaptiontexttotabname)|Определяет, отображает ли заголовок панели с вкладками тот же текст, что и активная вкладка. (переопределяет [CBaseTabbedPane:: кансеткаптионтексттотабнаме](../../mfc/reference/cbasetabbedpane-class.md#cansetcaptiontexttotabname).)|
|[CMFCOutlookBar:: Create](#create)|Создает элемент управления "панель Outlook".|
|[CMFCOutlookBar:: Креатекустомпаже](#createcustompage)|Создает настраиваемую вкладку панели Outlook.|
|`CMFCOutlookBar::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|[CMFCOutlookBar::D Оесалловдининсертбефоре](#doesallowdyninsertbefore)|Определяет, может ли пользователь закреплять панель элементов управления на внешнем крае панели Outlook.|
|[CMFCOutlookBar:: Флоаттаб](#floattab)|Перемещает панель, но только в том случае, если эта панель находится на вкладке, которая отсоединена. (переопределяет [CBaseTabbedPane:: флоаттаб](../../mfc/reference/cbasetabbedpane-class.md#floattab).)|
|[CMFCOutlookBar:: Жетбуттонсфонт](#getbuttonsfont)|Возвращает шрифт текста на кнопках панели Outlook.|
|[CMFCOutlookBar:: Жеттабареа](#gettabarea)|Возвращает размер и позицию областей вкладок на панели Outlook. (Переопределяет [CBaseTabbedPane:: жеттабареа](../../mfc/reference/cbasetabbedpane-class.md#gettabarea).)|
|`CMFCOutlookBar::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|
|[CMFCOutlookBar:: IsMode2003](#ismode2003)|Определяет, будет ли поведение панели Outlook имитироваться в Microsoft Office Outlook 2003 (см. примечания).|
|[CMFCOutlookBar::OnAfterAnimation](#onafteranimation)|Вызывается методом [кмфкаутлукбартабктрл:: сетактиветаб](../../mfc/reference/cmfcoutlookbartabctrl-class.md#setactivetab) после установки активной вкладки с помощью анимации.|
|[CMFCOutlookBar::OnBeforeAnimation](#onbeforeanimation)|Вызывается методом [кмфкаутлукбартабктрл:: сетактиветаб](../../mfc/reference/cmfcoutlookbartabctrl-class.md#setactivetab) , прежде чем страница вкладки задается как активная вкладка с помощью анимации.|
|[CMFCOutlookBar::OnScroll](#onscroll)|Вызывается платформой, если панель Outlook прокручивается вверх или вниз.|
|[CMFCOutlookBar:: Ремовекустомпаже](#removecustompage)|Удаляет вкладку настраиваемой панели Outlook.|
|[CMFCOutlookBar:: Сетбуттонсфонт](#setbuttonsfont)|Задает шрифт текста на кнопках на панели Outlook.|
|[CMFCOutlookBar:: SetMode2003](#setmode2003)|Указывает, будет ли поведение панели Outlook имитироваться для Outlook 2003 (см. примечания).|

## <a name="remarks"></a>Комментарии

Пример панели Outlook см. в примере [аутлукдемо: MFC Аутлукдемо Application](../../overview/visual-cpp-samples.md).

## <a name="implementing-the-outlook-bar"></a>Реализация панели Outlook

Для использования элемента управления `CMFCOutlookBar` в своем приложении выполните следующие действия:

1. Внедрите объект `CMFCOutlookBar` в класс окна главного фрейма.

    ```cpp
    class CMainFrame : public CMDIFrameWnd
    {
        // ...
        CMFCOutlookBar m_wndOutlookBar;
        CMFCOutlookBarPane m_wndOutlookPane;
        // ...
    };
    ```

1. При обработке сообщения WM_CREATE в главном фрейме вызовите метод [CMFCOutlookBar:: Create](#create) , чтобы создать элемент управления вкладки панели Outlook.

    ```cpp
    m_wndOutlookBar.Create (_T("Shortcuts"),
        this,
        CRect (0, 0, 100, 100),
        ID_VIEW_OUTLOOKBAR,
        WS_CHILD | WS_VISIBLE | CBRS_LEFT);
    ```

1. Получите указатель на базовый объект с `CMFCOutlookBarTabCtrl` помощью [CBaseTabbedPane:: жетундерлингвиндов](../../mfc/reference/cbasetabbedpane-class.md#getunderlyingwindow).

    ```cpp
    CMFCOutlookBarTabCtrl* pOutlookBar = (CMFCOutlookBarTabCtrl*) m_wndOutlookBar.GetUnderlyingWindow ();
    ```

1. Создайте объект [класса CMFCOutlookBarPane](../../mfc/reference/cmfcoutlookbarpane-class.md) для каждой вкладки, содержащей кнопки.

    ```cpp
    m_wndOutlookPane.Create(&m_wndOutlookBar,
        AFX_DEFAULT_TOOLBAR_STYLE,
        ID_OUTLOOK_PANE_GENERAL,
        AFX_CBRS_FLOAT | AFX_CBRS_RESIZE);

    // make the Outlook pane detachable (enable docking)
    m_wndOutlookPane.EnableDocking(CBRS_ALIGN_ANY);

    // add buttons
    m_wndOutlookPane.AddButton(theApp.LoadIcon (IDR_MAINFRAME),
        "About",
        ID_APP_ABOUT);

    m_wndOutlookPane.AddButton (theApp.LoadIcon (IDR_CUSTOM_OPEN_ICON),
        "Open",
        ID_FILE_OPEN);
    ```

1. Вызовите [кмфкаутлукбартабктрл:: аддтаб](../../mfc/reference/cmfcbasetabctrl-class.md#addtab) , чтобы добавить каждую новую вкладку. Задайте для параметра *бдетачабле* значение false, чтобы сделать страницу недоступной для отсоединения. Или используйте [кмфкаутлукбартабктрл:: аддконтрол](../../mfc/reference/cmfcoutlookbartabctrl-class.md#addcontrol) для добавления соединяемых страниц.

    ```cpp
    pOutlookBar->AddTab (&m_wndOutlookPane, "General", (UINT) -1, TRUE);
    ```

1. Чтобы добавить `CWnd` элемент управления, производный от (например, [класс кмфкшеллтриктрл](../../mfc/reference/cmfcshelltreectrl-class.md)), в качестве вкладки, создайте элемент управления и вызовите [кмфкаутлукбартабктрл:: аддтаб](../../mfc/reference/cmfcbasetabctrl-class.md#addtab) , чтобы добавить его на панель Outlook.

> [!NOTE]
> Следует использовать уникальные идентификаторы элементов управления для каждого объекта [класса CMFCOutlookBarPane](../../mfc/reference/cmfcoutlookbarpane-class.md) и для каждого `CWnd` объекта, производного от.

Чтобы динамически добавлять или удалять новые страницы во время выполнения, используйте [CMFCOutlookBar:: креатекустомпаже](#createcustompage) и [CMFCOutlookBar:: ремовекустомпаже](#removecustompage).

## <a name="outlook-2003-mode"></a>Режим Outlook 2003

В режиме Outlook 2003 кнопки на вкладке располагаются в нижней части панели Outlook. Если недостаточно места для отображения кнопок, они отображаются в виде значков в области, аналогичной панели инструментов, в нижней части панели.

Используйте [CMFCOutlookBar:: SetMode2003](#setmode2003) , чтобы включить режим Outlook 2003. Используйте [кмфкаутлукбартабктрл:: сеттулбаримажелист](../../mfc/reference/cmfcoutlookbartabctrl-class.md#settoolbarimagelist) , чтобы задать точечный рисунок, содержащий значки, отображаемые в нижней части панели Outlook. Значки в битовой карте должны упорядочиваться по индексу табуляции.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[CDockablePane](../../mfc/reference/cdockablepane-class.md)

[CBaseTabbedPane](../../mfc/reference/cbasetabbedpane-class.md)

[CMFCOutlookBar](../../mfc/reference/cmfcoutlookbar-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксаутлукбар. h

## <a name="cmfcoutlookbarallowdestroyemptytabbedpane"></a><a name="allowdestroyemptytabbedpane"></a> CMFCOutlookBar:: Алловдестройемптитаббедпане

Указывает, можно ли уничтожить пустую панель с вкладками.

```cpp
virtual BOOL AllowDestroyEmptyTabbedPane() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если пустая область с вкладками может быть удалена; в противном случае — значение FALSE. Реализация по умолчанию всегда возвращает значение TRUE.

### <a name="remarks"></a>Комментарии

Если пустая область с вкладками не может быть уничтожена, платформа скрывает ее.

## <a name="cmfcoutlookbarcanacceptpane"></a><a name="canacceptpane"></a> CMFCOutlookBar:: Канакцептпане

Определяет, можно ли прикрепить другую панель к панели Outlook.

```cpp
virtual BOOL CanAcceptPane(const CBasePane* pBar) const;
```

### <a name="parameters"></a>Параметры

*пбар*<br/>
окне Указатель на другую область, закрепленную на этой панели.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если другую панель можно закрепить на панели Outlook; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Если панель Outlook находится в режиме Outlook 2003, закрепление не поддерживается, поэтому возвращаемое значение равно FALSE.

Если параметр *пбар* имеет значение null, этот метод возвращает значение false.

В противном случае этот метод ведет себя как базовый метод [CBasePane:: канакцептпане](../../mfc/reference/cbasepane-class.md#canacceptpane), за исключением того, что даже в том случае, если закрепление не включено, панель Outlook может по-прежнему включать в себя закрепление другой панели Outlook.

## <a name="cmfcoutlookbarcansetcaptiontexttotabname"></a><a name="cansetcaptiontexttotabname"></a> CMFCOutlookBar:: Кансеткаптионтексттотабнаме

Определяет, отображает ли заголовок панели с вкладками тот же текст, что и активная вкладка.

```cpp
virtual BOOL CanSetCaptionTextToTabName() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если заголовок окна панели Outlook автоматически задается как текст активной вкладки; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Чтобы включить или отключить эту функцию, используйте [CBaseTabbedPane:: енаблесеткаптионтексттотабнаме](../../mfc/reference/cbasetabbedpane-class.md#enablesetcaptiontexttotabname) .

В режиме Outlook 2003 этот параметр всегда включен.

## <a name="cmfcoutlookbarcreate"></a><a name="create"></a> CMFCOutlookBar:: Create

Создает элемент управления "панель Outlook".

```cpp
virtual BOOL Create(
    LPCTSTR lpszCaption,
    CWnd* pParentWnd,
    const RECT& rect,
    UINT nID,
    DWORD dwStyle,
    DWORD dwControlBarStyle=AFX_CBRS_RESIZE,
    CCreateContext* pContext=NULL);
```

### <a name="parameters"></a>Параметры

*лпсзкаптион*<br/>
окне Задает заголовок окна.

*ппарентвнд*<br/>
окне Указывает указатель на родительское окно. Оно не должно иметь значение NULL.

*rect*<br/>
окне Задает размер и расположение панели Outlook в пикселях.

*nID*<br/>
окне Указывает идентификатор элемента управления. Должно отличаться от других идентификаторов элементов управления, используемых в приложении.

*двстиле*<br/>
окне Задает нужный стиль панели элементов управления. Возможные значения см. в разделе [стили окна](../../mfc/reference/styles-used-by-mfc.md#window-styles).

*двконтролбарстиле*<br/>
окне Задает специальные стили, определяемые библиотекой.

*pContext*<br/>
окне Создать контекст.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если метод успешно выполнен; в противном случае — 0.

### <a name="remarks"></a>Комментарии

`CMFCOutlookBar`Объект создается в два этапа. Сначала необходимо вызвать конструктор, а затем вызвать метод `Create` , который создает элемент управления "панель Outlook" и присоединяет его к `CMFCOutlookBar` объекту.

Список доступных стилей, определенных библиотекой, которые должны быть указаны в *двконтролбарстиле*, см. в разделе [CBasePane:: креатикс](../../mfc/reference/cbasepane-class.md#createex) .

### <a name="example"></a>Пример

В следующем примере показано, как использовать `Create` метод `CMFCOutlookBar` класса. Этот фрагмент кода является частью примера " [множественные представления Outlook](../../overview/visual-cpp-samples.md)".

[!code-cpp[NVC_MFC_OutlookMultiViews#1](../../mfc/reference/codesnippet/cpp/cmfcoutlookbar-class_1.h)]
[!code-cpp[NVC_MFC_OutlookMultiViews#2](../../mfc/reference/codesnippet/cpp/cmfcoutlookbar-class_2.cpp)]

## <a name="cmfcoutlookbarcreatecustompage"></a><a name="createcustompage"></a> CMFCOutlookBar:: Креатекустомпаже

Создает настраиваемую вкладку панели Outlook.

```cpp
CMFCOutlookBarPane* CreateCustomPage(
    LPCTSTR lpszPageName,
    BOOL bActivatePage=TRUE,
    DWORD dwEnabledDocking=CBRS_ALIGN_ANY,
    BOOL bEnableTextLabels=TRUE);
```

### <a name="parameters"></a>Параметры

*лпсзпаженаме*<br/>
окне Метка страницы.

*бактиватепаже*<br/>
окне Если значение — TRUE, страница активируется после создания.

*двенабледдоккинг*<br/>
окне Сочетание флагов CBRS_ALIGN_, определяющих включенные стороны стыковки при отсоединении страницы.

*бенаблетекстлабелс*<br/>
окне Если задано значение TRUE, то для кнопок, размещенных на странице, включены текстовые метки.

### <a name="return-value"></a>Возвращаемое значение

Указатель на только что созданную страницу или значение NULL в случае сбоя создания.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы разрешить пользователям создавать пользовательские страницы панели Outlook. Можно создать до 100 страниц для каждого приложения. Идентификаторы элементов управления страницы начинаются с число 0xF000 не. Создание завершается ошибкой, если общее число настраиваемых страниц панели Outlook превышает 100.

Для удаления настраиваемых страниц используйте [CMFCOutlookBar:: ремовекустомпаже](#removecustompage) .

## <a name="cmfcoutlookbardoesallowdyninsertbefore"></a><a name="doesallowdyninsertbefore"></a> CMFCOutlookBar::D Оесалловдининсертбефоре

Указывает, может ли пользователь закреплять панель на внешнем крае панели Outlook.

```
DECLARE_MESSAGE_MAP virtual BOOL DoesAllowDynInsertBefore() const;
```

### <a name="return-value"></a>Возвращаемое значение

Реализация по умолчанию возвращает значение FALSE.

### <a name="remarks"></a>Комментарии

Платформа вызывает `DoesAllowDynInsertBefore` метод при поиске расположения для закрепления динамической области. Если функция возвращает значение FALSE, платформа не разрешает закрепление любой динамической панели на внешних краях панели.

Как правило, панель Outlook создается как статический элемент управления без плавающего чтения. Эту функцию можно переопределить в производном классе и возвращать значение TRUE, чтобы изменить это поведение.

> [!NOTE]
> Так как динамические панели проверяют состояние закрепленных статических панелей при закреплении, динамические панели следует закреплять после статических панелей везде, где это возможно.

## <a name="cmfcoutlookbarfloattab"></a><a name="floattab"></a> CMFCOutlookBar:: Флоаттаб

Перемещает панель в плавающую область.

```cpp
virtual BOOL FloatTab(
    CWnd* pBar,
    int nTabID,
    AFX_DOCK_METHOD dockMethod,
    BOOL bHide);
```

### <a name="parameters"></a>Параметры

*пбар*<br/>
окне Указатель на область с плавающей запятой.

*нтабид*<br/>
окне Отсчитываемый от нуля индекс табуляции для перемещения.

*dockMethod*<br/>
окне Указывает метод, используемый, чтобы сделать панель плавающей.  Дополнительные сведения см. в разделе [CBaseTabbedPane:: флоаттаб](../../mfc/reference/cbasetabbedpane-class.md#floattab).

*bHide*<br/>
окне Значение TRUE, чтобы скрыть панель перед плавающей; в противном случае — значение FALSE. В отличие от версии этого метода базового класса этот параметр не имеет значения по умолчанию.

### <a name="return-value"></a>Возвращаемое значение

TRUE, если панель перемещена; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Этот метод похож на [CBaseTabbedPane:: флоаттаб](../../mfc/reference/cbasetabbedpane-class.md#floattab) , за исключением того, что в нем не включена последняя вкладка в элементе управления "панель Outlook" с плавающей запятой.

## <a name="cmfcoutlookbargetbuttonsfont"></a><a name="getbuttonsfont"></a> CMFCOutlookBar:: Жетбуттонсфонт

Возвращает шрифт текста на вкладках кнопки страницы в панели Outlook.

```cpp
CFont* GetButtonsFont() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на объект Font, используемый для показа текста на вкладках кнопок на странице панели Outlook.

### <a name="remarks"></a>Комментарии

Эта функция используется для извлечения шрифта, используемого для вывода текста на вкладках кнопки страницы Outlook. Шрифт можно задать, вызвав метод в [CMFCOutlookBar:: сетбуттонсфонт](#setbuttonsfont).

## <a name="cmfcoutlookbargettabarea"></a><a name="gettabarea"></a> CMFCOutlookBar:: Жеттабареа

Определяет размер и расположение областей вкладок на панели Outlook.

```cpp
virtual void GetTabArea(
    CRect& rectTabAreaTop,
    CRect& rectTabAreaBottom) const;
```

### <a name="parameters"></a>Параметры

*rectTabAreaTop*<br/>
заполняет Содержит размер и позицию (в клиентских координатах) области верхней вкладки при возврате функции.

*rectTabAreaBottom*<br/>
заполняет Содержит размер и позицию (в клиентских координатах) нижней области вкладки при возврате функции.

### <a name="remarks"></a>Комментарии

Платформа вызывает этот метод для определения типа закрепления на целевую панель. Когда платформа определяет, что пользователь перетаскивает панель, которая должна быть закреплена за областью вкладки целевой области, она пытается добавить первую панель в качестве новой вкладки целевой области. В противном случае он пытается закрепить первую панель на соответствующей стороне целевой области. Платформа создает новый контейнер с ползунком для размещения дополнительной закрепленной панели.

Реализация по умолчанию `GetTabArea` возвращает всю клиентскую область панели Outlook, если панель Outlook является статической, то есть если панель Outlook не может перемещаться. В противном случае она возвращает область, которую кнопки страницы занимают сверху и снизу элемента управления "панель Outlook".

Чтобы изменить это поведение, Переопределите этот метод в классе, производном от `CMFCOutlookBar` .

## <a name="cmfcoutlookbarismode2003"></a><a name="ismode2003"></a> CMFCOutlookBar:: IsMode2003

Указывает, будет ли поведение панели Outlook имитироваться в Microsoft Office Outlook 2003.

```cpp
BOOL IsMode2003() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если панель Outlook работает в режиме Microsoft Office 2003. в противном случае — 0.

### <a name="remarks"></a>Комментарии

Этот режим можно включить с помощью [CMFCOutlookBar:: SetMode2003](#setmode2003).

## <a name="cmfcoutlookbaronafteranimation"></a><a name="onafteranimation"></a> CMFCOutlookBar:: Онафтераниматион

Вызывается методом [кмфкаутлукбартабктрл:: сетактиветаб](../../mfc/reference/cmfcoutlookbartabctrl-class.md#setactivetab) после установки активной вкладки с помощью анимации.

```cpp
virtual void OnAfterAnimation(int nPage);
```

### <a name="parameters"></a>Параметры

*нпаже*<br/>
окне Отсчитываемый от нуля индекс страницы вкладки, которая была сделана активной.

### <a name="remarks"></a>Комментарии

Визуальный эффект настройки активной вкладки зависит от того, включена ли анимация. Дополнительные сведения см. в разделе [кмфкаутлукбартабктрл:: енаблеаниматион](../../mfc/reference/cmfcoutlookbartabctrl-class.md#enableanimation).

## <a name="cmfcoutlookbaronbeforeanimation"></a><a name="onbeforeanimation"></a> CMFCOutlookBar:: Онбефореаниматион

Вызывается методом [кмфкаутлукбартабктрл:: сетактиветаб](../../mfc/reference/cmfcoutlookbartabctrl-class.md#setactivetab) , прежде чем страница вкладки задается как активная вкладка с помощью анимации.

```cpp
virtual BOOL OnBeforeAnimation(int nPage);
```

### <a name="parameters"></a>Параметры

*нпаже*<br/>
окне Отсчитываемый от нуля индекс страницы вкладки, которая должна быть задана как активная.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если анимация используется при настройке новой активной вкладки, или значение FALSE, если анимация должна быть отключена.

### <a name="remarks"></a>Комментарии

## <a name="cmfcoutlookbaronscroll"></a><a name="onscroll"></a> CMFCOutlookBar:: OnScroll

Вызывается платформой, если панель Outlook прокручивается вверх или вниз.

```cpp
virtual void OnScroll(BOOL bDown);
```

### <a name="parameters"></a>Параметры

*бдовн*<br/>
окне Значение TRUE, если панель Outlook прокручивается вниз, или значение FALSE, если выполняется прокрутка.

### <a name="remarks"></a>Комментарии

## <a name="cmfcoutlookbarremovecustompage"></a><a name="removecustompage"></a> CMFCOutlookBar:: Ремовекустомпаже

Удаляет настраиваемую страницу вкладки Outlook.

```cpp
BOOL RemoveCustomPage(
    UINT uiPage,
    CMFCOutlookBarTabCtrl* pTargetWnd);
```

### <a name="parameters"></a>Параметры

*Страницу uipage*<br/>
окне Отсчитываемый от нуля индекс страницы в родительском окне Outlook.

*птаржетвнд*<br/>
окне Поинтерто родительское окно Outlook.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если пользовательская страница успешно удалена; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы удалить пользовательские страницы. При удалении страницы ее идентификатор элемента управления возвращается в пул доступных идентификаторов.

Необходимо указать указатель на объект [класса кмфкаутлукбартабктрл](../../mfc/reference/cmfcoutlookbartabctrl-class.md) , в котором в данный момент удаляется страница. Обратите внимание, что пользователь может перемещать отсоединяемые страницы между разными панелями Outlook, но сведения о пользовательской странице находятся в объекте панели Outlook, для которого вы вызвали [CMFCOutlookBar:: креатекустомпаже](#createcustompage).

Чтобы получить указатель на окно Outlook, используйте [CBaseTabbedPane:: жетундерлингвиндов](../../mfc/reference/cbasetabbedpane-class.md#getunderlyingwindow) .

## <a name="cmfcoutlookbarsetbuttonsfont"></a><a name="setbuttonsfont"></a> CMFCOutlookBar:: Сетбуттонсфонт

Задает шрифт текста на кнопках на панели Outlook.

```cpp
void SetButtonsFont(
    CFont* pFont,
    BOOL bRedraw=TRUE);
```

### <a name="parameters"></a>Параметры

*пфонт*<br/>
окне Указывает новый шрифт.

*bRedraw*<br/>
окне Если значение — TRUE, панель Outlook будет перерисована.

### <a name="remarks"></a>Комментарии

Этот метод используется для установки шрифта текста, отображаемого на кнопках страницы вкладки Outlook.

## <a name="cmfcoutlookbarsetmode2003"></a><a name="setmode2003"></a> CMFCOutlookBar:: SetMode2003

Указывает, будет ли поведение панели Outlook имитироваться для Outlook 2003.

```cpp
void SetMode2003(BOOL bMode2003=TRUE);
```

### <a name="parameters"></a>Параметры

*bMode2003*<br/>
окне Если задано значение TRUE, то режим Office 2003 включен.

### <a name="remarks"></a>Комментарии

Эта функция используется для включения или отключения режима Office 2003. В этом режиме панель Outlook содержит дополнительную панель инструментов с кнопкой настройки. Поведение панели Outlook соответствует поведению панели Outlook в Microsoft Office 2003.

По умолчанию этот режим отключен.

> [!NOTE]
> Эта функция должна вызываться до [CMFCOutlookBar:: Create](#create).

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CBaseTabbedPane](../../mfc/reference/cbasetabbedpane-class.md)<br/>
[Класс Кмфкаутлукбартабктрл](../../mfc/reference/cmfcoutlookbartabctrl-class.md)<br/>
[Класс CMFCOutlookBarPane](../../mfc/reference/cmfcoutlookbarpane-class.md)
