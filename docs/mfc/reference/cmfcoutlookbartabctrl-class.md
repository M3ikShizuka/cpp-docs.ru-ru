---
description: 'Дополнительные сведения о: Кмфкаутлукбартабктрл Class'
title: CMFCOutlookBarTabCtrl Class
ms.date: 10/18/2018
f1_keywords:
- CMFCOutlookBarTabCtrl
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::AddControl
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::CanShowFewerPageButtons
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::CanShowMorePageButtons
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::Create
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::EnableAnimation
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::EnableInPlaceEdit
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::EnableScrollButtons
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::GetBorderSize
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::GetVisiblePageButtons
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::IsAnimation
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::IsMode2003
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::OnShowFewerPageButtons
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::OnShowMorePageButtons
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::OnShowOptions
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::SetActiveTab
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::SetBorderSize
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::SetPageButtonTextAlign
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::SetToolbarImageList
- AFXOUTLOOKBARTABCTRL/CMFCOutlookBarTabCtrl::SetVisiblePageButtons
helpviewer_keywords:
- CMFCOutlookBarTabCtrl [MFC], AddControl
- CMFCOutlookBarTabCtrl [MFC], CanShowFewerPageButtons
- CMFCOutlookBarTabCtrl [MFC], CanShowMorePageButtons
- CMFCOutlookBarTabCtrl [MFC], Create
- CMFCOutlookBarTabCtrl [MFC], EnableAnimation
- CMFCOutlookBarTabCtrl [MFC], EnableInPlaceEdit
- CMFCOutlookBarTabCtrl [MFC], EnableScrollButtons
- CMFCOutlookBarTabCtrl [MFC], GetBorderSize
- CMFCOutlookBarTabCtrl [MFC], GetVisiblePageButtons
- CMFCOutlookBarTabCtrl [MFC], IsAnimation
- CMFCOutlookBarTabCtrl [MFC], IsMode2003
- CMFCOutlookBarTabCtrl [MFC], OnShowFewerPageButtons
- CMFCOutlookBarTabCtrl [MFC], OnShowMorePageButtons
- CMFCOutlookBarTabCtrl [MFC], OnShowOptions
- CMFCOutlookBarTabCtrl [MFC], SetActiveTab
- CMFCOutlookBarTabCtrl [MFC], SetBorderSize
- CMFCOutlookBarTabCtrl [MFC], SetPageButtonTextAlign
- CMFCOutlookBarTabCtrl [MFC], SetToolbarImageList
- CMFCOutlookBarTabCtrl [MFC], SetVisiblePageButtons
ms.assetid: b1f2b3f7-cc59-49a3-99d8-7ff9b37c044b
ms.openlocfilehash: b969fbb592fc3098dc8d287004fab90da6f30111
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333502"
---
# <a name="cmfcoutlookbartabctrl-class"></a>CMFCOutlookBarTabCtrl Class

Элемент управления "вкладка", который имеет внешний вид раздела **Область переходов** в Microsoft Outlook.
Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMFCOutlookBarTabCtrl : public CMFCBaseTabCtrl
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCOutlookBarTabCtrl::CMFCOutlookBarTabCtrl`|Конструктор по умолчанию.|
|`CMFCOutlookBarTabCtrl::~CMFCOutlookBarTabCtrl`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкаутлукбартабктрл:: Аддконтрол](#addcontrol)|Добавляет элемент управления Windows в качестве новой вкладки на панели Outlook.|
|`CMFCOutlookBarTabCtrl::CalcRectEdit`|Вызывается платформой для определения размеров поля редактирования, которое появляется при переименовании вкладки пользователем. (Overrides `CMFCBaseTabCtrl::CalcRectEdit` .)|
|[Кмфкаутлукбартабктрл:: Каншовфеверпажебуттонс](#canshowfewerpagebuttons)|Вызывается платформой во время операций изменения размера, чтобы определить, может ли быть отображено меньшее количество кнопок на вкладке панели Outlook, чем доступно в настоящий момент.|
|[Кмфкаутлукбартабктрл:: Каншовморепажебуттонс](#canshowmorepagebuttons)|Вызывается платформой во время операций изменения размера, чтобы определить, могут ли отображаться дополнительные кнопки страницы вкладки панели Outlook, чем видимые в данный момент.|
|[Кмфкаутлукбартабктрл:: Create](#create)|Создает элемент управления вкладки панели Outlook.|
|`CMFCOutlookBarTabCtrl::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|[Кмфкаутлукбартабктрл:: Енаблеаниматион](#enableanimation)|Указывает, включена ли анимация, которая происходит во время переключения между активными вкладками.|
|[Кмфкаутлукбартабктрл:: Енаблеинплацеедит](#enableinplaceedit)|Указывает, может ли пользователь изменять текстовые метки на кнопках вкладки панели Outlook. (Переопределяет [CMFCBaseTabCtrl:: енаблеинплацеедит](../../mfc/reference/cmfcbasetabctrl-class.md#enableinplaceedit).)|
|[Кмфкаутлукбартабктрл:: Енаблескроллбуттонс](#enablescrollbuttons)|Вызывается платформой для включения кнопок, позволяющих пользователю выполнять прокрутку кнопок панели Outlook.|
|`CMFCOutlookBarTabCtrl::FindTargetWnd`|Определяет область, которая содержит указанную точку. (Переопределяет [CMFCBaseTabCtrl:: финдтаржетвнд](../../mfc/reference/cmfcbasetabctrl-class.md#findtargetwnd).)|
|[Кмфкаутлукбартабктрл:: Жетбордерсизе](#getbordersize)|Возвращает размер границы элемента управления вкладки Outlook.|
|`CMFCOutlookBarTabCtrl::GetTabArea`|Извлекает размер и положение области вкладки набора вкладок. (Переопределяет [CMFCBaseTabCtrl:: жеттабареа](../../mfc/reference/cmfcbasetabctrl-class.md#gettabarea).)|
|`CMFCOutlookBarTabCtrl::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|
|[Кмфкаутлукбартабктрл:: Жетвисиблепажебуттонс](#getvisiblepagebuttons)||
|[Кмфкаутлукбартабктрл:: Animation](#isanimation)|Определяет, включена ли анимация, которая происходит во время переключения между активными вкладками.|
|[Кмфкаутлукбартабктрл:: IsMode2003](#ismode2003)|Определяет, находится ли элемент управления вкладки панели Outlook в режиме, который эмулирует Microsoft Outlook 2003.|
|`CMFCOutlookBarTabCtrl::IsPtInTabArea`|Определяет, находится ли точка внутри области вкладок. (Переопределяет [CMFCBaseTabCtrl:: исптинтабареа](../../mfc/reference/cmfcbasetabctrl-class.md#isptintabarea).)|
|`CMFCOutlookBarTabCtrl::IsTabDetachable`|Указывает, является ли вкладка отделяемой. (Переопределяет [CMFCBaseTabCtrl:: истабдетачабле](../../mfc/reference/cmfcbasetabctrl-class.md#istabdetachable).)|
|`CMFCOutlookBarTabCtrl::OnChangeTabs`|Вызывается структурой при вставке или удалении вкладки. (Переопределяет `CMFCBaseTabCtrl::OnChangeTabs`.)|
|[Кмфкаутлукбартабктрл:: Оншовфеверпажебуттонс](#onshowfewerpagebuttons)|Вызывается платформой для уменьшения числа видимых кнопок на странице вкладок.|
|[Кмфкаутлукбартабктрл:: Оншовморепажебуттонс](#onshowmorepagebuttons)|Вызывается платформой для увеличения числа видимых кнопок на странице вкладок.|
|[Кмфкаутлукбартабктрл:: Оншовоптионс](#onshowoptions)|Отображает диалоговое окно **Параметры области навигации** .|
|`CMFCOutlookBarTabCtrl::RecalcLayout`|Повторно вычисляет внутренний макет набора вкладок. (Переопределяет [CMFCBaseTabCtrl:: RecalcLayout](../../mfc/reference/cmfcbasetabctrl-class.md#recalclayout).)|
|[Кмфкаутлукбартабктрл:: Сетактиветаб](#setactivetab)|Задает активную вкладку. (переопределяет [CMFCBaseTabCtrl:: сетактиветаб](../../mfc/reference/cmfcbasetabctrl-class.md#setactivetab).)|
|[Кмфкаутлукбартабктрл:: Сетбордерсизе](#setbordersize)|Задает размер границы элемента управления вкладки Outlook.|
|[Кмфкаутлукбартабктрл:: Сетпажебуттонтексталигн](#setpagebuttontextalign)|Задает выравнивание текстовых меток на кнопках вкладки на панели Outlook.|
|[Кмфкаутлукбартабктрл:: Сеттулбаримажелист](#settoolbarimagelist)|Задает точечный рисунок, содержащий значки, которые отображаются в нижней части панели Outlook в режиме Outlook 2003 (см. [Класс CMFCOutlookBar](../../mfc/reference/cmfcoutlookbar-class.md)).|
|[Кмфкаутлукбартабктрл:: Сетвисиблепажебуттонс](#setvisiblepagebuttons)||

## <a name="remarks"></a>Комментарии

Чтобы создать панель Outlook с поддержкой закрепления, используйте `CMFCOutlookBar` объект для размещения элемента управления вкладки панели Outlook. Дополнительные сведения см. в разделе [Класс CMFCOutlookBar](../../mfc/reference/cmfcoutlookbar-class.md).

## <a name="example"></a>Пример

В следующем примере показано, как инициализировать `CMFCOutlookBarTabCtrl` объект и использовать различные методы в `CMFCOutlookBarTabCtrl` классе. В примере показано, как включить редактирование на месте текстовой метки на кнопках вкладки панели Outlook, включить анимацию, включить маркеры прокрутки, позволяющие пользователю прокручивать кнопки на панели Outlook, задавать размер границы элемента управления вкладки Outlook и устанавливать выравнивание текстовых меток на кнопках вкладки на панели Outlook. Этот фрагмент кода является частью [демонстрационного примера Outlook](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_OutlookDemo#1](../../mfc/reference/codesnippet/cpp/cmfcoutlookbartabctrl-class_1.cpp)]
[!code-cpp[NVC_MFC_OutlookDemo#2](../../mfc/reference/codesnippet/cpp/cmfcoutlookbartabctrl-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CMFCBaseTabCtrl](../../mfc/reference/cmfcbasetabctrl-class.md)

[CMFCOutlookBarTabCtrl](../../mfc/reference/cmfcoutlookbartabctrl-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксаутлукбартабктрл. h

## <a name="cmfcoutlookbartabctrladdcontrol"></a><a name="addcontrol"></a> Кмфкаутлукбартабктрл:: Аддконтрол

Добавляет элемент управления Windows в качестве новой вкладки на панели Outlook.

```cpp
void AddControl(
    CWnd* pWndCtrl,
    LPCTSTR lpszName,
    int nImageID=-1,
    BOOL bDetachable=TRUE,
    DWORD dwControlBarStyle=AFX_CBRS_FLOAT |  AFX_CBRS_CLOSE | AFX_CBRS_RESIZE |  CBRS_AFX_AUTOHIDE);
```

### <a name="parameters"></a>Параметры

*пвндктрл*<br/>
окне Указатель на добавляемый элемент управления.

*лпсзнаме*<br/>
окне Указывает имя вкладки.

*bDetachable*<br/>
окне Если значение — TRUE, страница будет создана как отсоединяемая.

*нимажеид*<br/>
окне Индекс изображения во внутреннем списке изображений для изображения, отображаемого на новой вкладке.

*двконтролбарстиле*<br/>
окне Задает стиль AFX_ CBRS_ * для закрепленных панелей закрепления.

### <a name="remarks"></a>Комментарии

Эта функция используется для добавления элемента управления в качестве новой страницы панели Outlook.

Эта функция внутренне вызывает метод в [CMFCBaseTabCtrl:: аддтаб](../../mfc/reference/cmfcbasetabctrl-class.md#addtab).

Если параметру *бдетачабле* присвоить значение true, `AddControl` внутренне создает `CDockablePaneAdapter` объект и заключает в оболочку добавленный элемент управления. Он автоматически задает классу среды выполнения окна с вкладками класс среды выполнения, `CMFCOutlookBar` а классу среды выполнения для плавающей рамки — значение `CMultiPaneFrameWnd` .

### <a name="example"></a>Пример

В следующем примере показано, как использовать `AddControl` метод в `CMFCOutlookBarTabCtrl` классе. Этот фрагмент кода является частью [демонстрационного примера Outlook](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_OutlookDemo#3](../../mfc/reference/codesnippet/cpp/cmfcoutlookbartabctrl-class_3.cpp)]

## <a name="cmfcoutlookbartabctrlcanshowfewerpagebuttons"></a><a name="canshowfewerpagebuttons"></a> Кмфкаутлукбартабктрл:: Каншовфеверпажебуттонс

Вызывается платформой во время операций изменения размера, чтобы определить, может ли быть отображено меньшее количество кнопок на вкладке панели Outlook, чем доступно в настоящий момент.

```
virtual BOOL CanShowFewerPageButtons() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если имеется более одной кнопки; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Элемент управления "панель Outlook" динамически добавляет или удаляет вкладки из отображения в зависимости от того, сколько свободного места доступно. Этот метод используется платформой для помощи в этом процессе.

## <a name="cmfcoutlookbartabctrlcanshowmorepagebuttons"></a><a name="canshowmorepagebuttons"></a> Кмфкаутлукбартабктрл:: Каншовморепажебуттонс

Вызывается платформой во время операций изменения размера, чтобы определить, могут ли отображаться дополнительные кнопки страницы вкладки Outlook, чем видимые в данный момент.

```
virtual BOOL CanShowMorePageButtons() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если имеются кнопки, которые в данный момент не видны; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Элемент управления "панель Outlook" динамически добавляет или удаляет вкладки из отображения в зависимости от того, сколько свободного места доступно. Этот метод используется платформой для помощи в этом процессе.

## <a name="cmfcoutlookbartabctrlcreate"></a><a name="create"></a> Кмфкаутлукбартабктрл:: Create

Создает элемент управления вкладки панели Outlook.

```
virtual BOOL Create(
    const CRect& rect,
    CWnd* pParentWnd,
    UINT nID);
```

### <a name="parameters"></a>Параметры

*rect*<br/>
окне Задает начальный размер и расположение в пикселях.

*ппарентвнд*<br/>
окне Указывает на родительское окно. Не может иметь значение NULL.

*nID*<br/>
окне Идентификатор элемента управления.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если элемент управления успешно создан; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Обычно элементы управления "панель Outlook" создаются, когда [Класс CMFCOutlookBar](../../mfc/reference/cmfcoutlookbar-class.md) управляет сообщением WM_CREATE процесса.

## <a name="cmfcoutlookbartabctrlenableanimation"></a><a name="enableanimation"></a> Кмфкаутлукбартабктрл:: Енаблеаниматион

Указывает, включена ли анимация, которая происходит во время переключения между активными вкладками.

```
static void EnableAnimation(BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
окне Указывает, должна ли быть включена или отключена анимация.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы включить и отключить анимацию. Когда пользователь открывает страницу вкладки, заголовок страницы отображается на слайдах вверх или вниз, если включена анимация. Если анимация отключена, страница немедленно становится активной.

По умолчанию анимация включена.

## <a name="cmfcoutlookbartabctrlenableinplaceedit"></a><a name="enableinplaceedit"></a> Кмфкаутлукбартабктрл:: Енаблеинплацеедит

Указывает, может ли пользователь изменять текстовые метки на кнопках вкладки на панели Outlook.

```
virtual void EnableInPlaceEdit(BOOL bEnable);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
Если значение — TRUE, включите редактирование на месте текстовой метки. Если значение равно FALSE, отключите редактирование на месте.

### <a name="remarks"></a>Комментарии

Эта функция вызывается для включения или отключения редактирования текстовых меток на панели вкладок на месте. По умолчанию редактирование на месте отключено.

## <a name="cmfcoutlookbartabctrlenablescrollbuttons"></a><a name="enablescrollbuttons"></a> Кмфкаутлукбартабктрл:: Енаблескроллбуттонс

Вызывается платформой для включения маркеров прокрутки, позволяющих пользователю прокручивать кнопки на панели Outlook.

```cpp
void EnableScrollButtons(
    BOOL bEnable = TRUE,
    BOOL bIsUp = TRUE,
    BOOL bIsDown = TRUE);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
окне Определяет, отображаются ли кнопки прокрутки.

*бисуп*<br/>
окне Определяет, отображается ли верхняя полоса прокрутки.

*бисдовн*<br/>
окне Определяет, отображается ли нижняя полоса прокрутки.

### <a name="remarks"></a>Комментарии

Включает отображение кнопок прокрутки. Этот метод вызывается платформой при изменении активной вкладки для восстановления кнопок прокрутки.

## <a name="cmfcoutlookbartabctrlgetbordersize"></a><a name="getbordersize"></a> Кмфкаутлукбартабктрл:: Жетбордерсизе

Возвращает размер границы элемента управления вкладки Outlook.

```
int GetBorderSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Размер границы в пикселях.

## <a name="cmfcoutlookbartabctrlgetvisiblepagebuttons"></a><a name="getvisiblepagebuttons"></a> Кмфкаутлукбартабктрл:: Жетвисиблепажебуттонс

```
int GetVisiblePageButtons() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcoutlookbartabctrlisanimation"></a><a name="isanimation"></a> Кмфкаутлукбартабктрл:: Animation

Указывает, включена ли анимация, которая происходит во время переключения между активными вкладками.

```
static BOOL IsAnimation();
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если анимация включена. в противном случае — 0.

### <a name="remarks"></a>Комментарии

Вызовите функцию [кмфкаутлукбартабктрл:: енаблеаниматион](#enableanimation) , чтобы включить или отключить анимацию.

## <a name="cmfcoutlookbartabctrlismode2003"></a><a name="ismode2003"></a> Кмфкаутлукбартабктрл:: IsMode2003

Определяет, находится ли элемент управления "панель Outlook" в режиме, который эмулирует Microsoft Outlook 2003.

```
BOOL IsMode2003() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если элемент управления вкладки панели Outlook находится в режиме Outlook 2003. в противном случае FALSE;

### <a name="remarks"></a>Комментарии

Это значение задается параметром [CMFCOutlookBar:: SetMode2003](../../mfc/reference/cmfcoutlookbar-class.md#setmode2003).

## <a name="cmfcoutlookbartabctrlonshowfewerpagebuttons"></a><a name="onshowfewerpagebuttons"></a> Кмфкаутлукбартабктрл:: Оншовфеверпажебуттонс

Вызывается платформой для уменьшения числа видимых кнопок на странице вкладок.

```
virtual void OnShowFewerPageButtons();
```

### <a name="remarks"></a>Комментарии

Этот метод корректирует количество видимых кнопок вкладки страницы при изменении размера элемента управления.

## <a name="cmfcoutlookbartabctrlonshowmorepagebuttons"></a><a name="onshowmorepagebuttons"></a> Кмфкаутлукбартабктрл:: Оншовморепажебуттонс

Вызывается платформой для увеличения числа видимых кнопок на странице вкладок.

```
virtual void OnShowMorePageButtons();
```

### <a name="remarks"></a>Комментарии

Этот метод позволяет изменить количество кнопок на странице вкладок, отображаемых при изменении размера элемента управления.

## <a name="cmfcoutlookbartabctrlonshowoptions"></a><a name="onshowoptions"></a> Кмфкаутлукбартабктрл:: Оншовоптионс

Отображает диалоговое окно **Параметры области навигации** .

```
virtual void OnShowOptions();
```

### <a name="remarks"></a>Комментарии

Диалоговое окно **Параметры области навигации** позволяет пользователю выбирать, какие кнопки страницы вкладки должны отображаться, и порядок их отображения.

Этот метод вызывается платформой, когда пользователь выбирает пункт меню **Параметры области навигации** в меню настройки элемента управления.

## <a name="cmfcoutlookbartabctrlsetactivetab"></a><a name="setactivetab"></a> Кмфкаутлукбартабктрл:: Сетактиветаб

Задает активную вкладку. Активная вкладка является открытой и отображается ее содержимое.

```
virtual BOOL SetActiveTab(int iTab);
```

### <a name="parameters"></a>Параметры

*iTab*<br/>
окне Отсчитываемый от нуля индекс вкладки, который необходимо открыть.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если указанная вкладка успешно открыта. в противном случае — 0.

### <a name="remarks"></a>Комментарии

Визуальный эффект настройки активной вкладки зависит от того, включена ли анимация. Дополнительные сведения см. в разделе [кмфкаутлукбартабктрл:: енаблеаниматион](#enableanimation).

## <a name="cmfcoutlookbartabctrlsetbordersize"></a><a name="setbordersize"></a> Кмфкаутлукбартабктрл:: Сетбордерсизе

Задает размер границы элемента управления вкладки Outlook.

```cpp
void SetBorderSize(int nBorderSize);
```

### <a name="parameters"></a>Параметры

*нбордерсизе*<br/>
окне Задает новый размер границы в пикселях.

### <a name="remarks"></a>Комментарии

Задает новый размер границы и пересчитывает макет окна Outlook.

## <a name="cmfcoutlookbartabctrlsetpagebuttontextalign"></a><a name="setpagebuttontextalign"></a> Кмфкаутлукбартабктрл:: Сетпажебуттонтексталигн

Задает выравнивание текстовых меток на кнопках вкладки на панели Outlook.

```cpp
void SetPageButtonTextAlign(
    UINT uiAlign,
    BOOL bRedraw=TRUE);
```

### <a name="parameters"></a>Параметры

*уиалигн*<br/>
окне Задает выравнивание текста.

*bRedraw*<br/>
окне Если значение — TRUE, окно Outlook будет перерисовано.

### <a name="remarks"></a>Комментарии

Эта функция используется для изменения выравнивания текста для кнопок страницы.

*уиалигн* может иметь одно из следующих значений:

|Константа|Значение|
|--------------|-------------|
|TA_LEFT|Выравнивание по левому краю|
|TA_CENTER|Выравнивание по центру|
|TA_RIGHT|Выравнивание по правому краю|

Значение по умолчанию — TA_CENTER.

## <a name="cmfcoutlookbartabctrlsettoolbarimagelist"></a><a name="settoolbarimagelist"></a> Кмфкаутлукбартабктрл:: Сеттулбаримажелист

Задает точечный рисунок, содержащий значки, которые отображаются в нижней части панели Outlook в режиме Outlook 2003.

```
BOOL SetToolbarImageList(
    UINT uiID,
    int cx,
    COLORREF clrTransp=RGB(255, 0, 255));
```

### <a name="parameters"></a>Параметры

*uiID*<br/>
окне Указывает идентификатор ресурса загружаемого образа.

*/CX*<br/>
окне Задает ширину изображения в списке изображений в пикселях.

*clrTransp*<br/>
окне Значение RGB, указывающее прозрачный цвет.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE в случае успешного выполнения. в противном случае возвращает значение FALSE.

### <a name="remarks"></a>Комментарии

Эта функция используется для присоединения списка изображений, изображения которого будут отображаться на кнопках панели инструментов в режиме Microsoft Office 2003. Индексы изображений должны соответствовать индексам страниц.

Этот метод не должен вызываться, если не находится в режиме Microsoft Office 2003. Дополнительные сведения см. в разделе [Класс CMFCOutlookBar](../../mfc/reference/cmfcoutlookbar-class.md).

## <a name="cmfcoutlookbartabctrlsetvisiblepagebuttons"></a><a name="setvisiblepagebuttons"></a> Кмфкаутлукбартабктрл:: Сетвисиблепажебуттонс

```cpp
void SetVisiblePageButtons(int nVisiblePageButtons);
```

### <a name="parameters"></a>Параметры

окне *нвисиблепажебуттонс*<br/>

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCBaseTabCtrl](../../mfc/reference/cmfcbasetabctrl-class.md)<br/>
[Класс CMFCOutlookBar](../../mfc/reference/cmfcoutlookbar-class.md)<br/>
[Класс CMFCOutlookBarPane](../../mfc/reference/cmfcoutlookbarpane-class.md)
