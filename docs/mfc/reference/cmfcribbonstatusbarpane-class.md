---
description: 'Дополнительные сведения о: CMFCRibbonStatusBarPane Class'
title: Класс CMFCRibbonStatusBarPane
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonStatusBarPane
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::CMFCRibbonStatusBarPane
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::GetAlmostLargeText
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::GetTextAlign
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::IsAnimation
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::IsExtended
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::OnDrawBorder
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::OnFillBackground
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::SetAlmostLargeText
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::SetAnimationList
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::SetTextAlign
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::StartAnimation
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::StopAnimation
- AFXRIBBONSTATUSBARPANE/CMFCRibbonStatusBarPane::OnFinishAnimation
helpviewer_keywords:
- CMFCRibbonStatusBarPane [MFC], CMFCRibbonStatusBarPane
- CMFCRibbonStatusBarPane [MFC], GetAlmostLargeText
- CMFCRibbonStatusBarPane [MFC], GetTextAlign
- CMFCRibbonStatusBarPane [MFC], IsAnimation
- CMFCRibbonStatusBarPane [MFC], IsExtended
- CMFCRibbonStatusBarPane [MFC], OnDrawBorder
- CMFCRibbonStatusBarPane [MFC], OnFillBackground
- CMFCRibbonStatusBarPane [MFC], SetAlmostLargeText
- CMFCRibbonStatusBarPane [MFC], SetAnimationList
- CMFCRibbonStatusBarPane [MFC], SetTextAlign
- CMFCRibbonStatusBarPane [MFC], StartAnimation
- CMFCRibbonStatusBarPane [MFC], StopAnimation
- CMFCRibbonStatusBarPane [MFC], OnFinishAnimation
ms.assetid: 5d034c3c-ecca-4267-b88c-0f55a2884dd0
ms.openlocfilehash: 4ddbee5a6c44411ef2ac34bff3e07b47c3d950a0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264990"
---
# <a name="cmfcribbonstatusbarpane-class"></a>Класс CMFCRibbonStatusBarPane

`CMFCRibbonStatusBarPane`Класс реализует элемент Ribbon, который можно добавить в строку состояния ленты.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonStatusBarPane : public CMFCRibbonButton
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonStatusBarPane:: CMFCRibbonStatusBarPane](#cmfcribbonstatusbarpane)|Создает и инициализирует объект `CMFCRibbonStatusBarPane`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonStatusBarPane:: Жеталмостларжетекст](#getalmostlargetext)|Возвращает строку, которая определяет длинную текстовую строку, которая может отображаться на панели без усечения.|
|[CMFCRibbonStatusBarPane:: Жеттексталигн](#gettextalign)|Возвращает текущее значение выравнивания текста.|
|[CMFCRibbonStatusBarPane:: Animation](#isanimation)|Определяет, выполняется ли анимация.|
|[CMFCRibbonStatusBarPane:: Extended](#isextended)|Определяет, находится ли панель в расширенной области строки состояния ленты.|
|[CMFCRibbonStatusBarPane:: Ондравбордер](#ondrawborder)|(Переопределяет [CMFCRibbonButton:: ондравбордер](../../mfc/reference/cmfcribbonbutton-class.md#ondrawborder).)|
|[CMFCRibbonStatusBarPane:: Онфиллбаккграунд](#onfillbackground)|(Переопределяет [CMFCRibbonButton:: онфиллбаккграунд](../../mfc/reference/cmfcribbonbutton-class.md#onfillbackground).)|
|[CMFCRibbonStatusBarPane:: Сеталмостларжетекст](#setalmostlargetext)|Определяет самую длинную текстовую строку, которая может отображаться на панели без усечения.|
|[CMFCRibbonStatusBarPane:: Сетаниматионлист](#setanimationlist)|Присваивает панели список изображений, который можно использовать для анимации.|
|[CMFCRibbonStatusBarPane:: Сеттексталигн](#settextalign)|Задает выравнивание текста.|
|[CMFCRibbonStatusBarPane:: Стартаниматион](#startanimation)|Запускает анимацию, назначенную панели.|
|[CMFCRibbonStatusBarPane:: Стопаниматион](#stopanimation)|Останавливает анимацию, назначенную панели. .|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CMFCRibbonStatusBarPane:: Онфинишаниматион](#onfinishanimation)|Вызывается структурой при остановке анимации, назначенной панели.|

## <a name="example"></a>Пример

В следующем примере демонстрируется использование различных методов класса `CMFCRibbonStatusBarPane`. В этом примере показано, как создать `CMFCRibbonStatusBarPane` объект, задать выравнивание текста метки на панели строки состояния, определить самый длинный текст, который может отображаться на панели строки состояния без усечения, присоединиться к панели строки состояния список изображений, который можно использовать для анимации, и запустить анимацию.

[!code-cpp[NVC_MFC_RibbonApp#2](../../mfc/reference/codesnippet/cpp/cmfcribbonstatusbarpane-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)

[CMFCRibbonStatusBarPane](../../mfc/reference/cmfcribbonstatusbarpane-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонстатусбарпане. h

## <a name="cmfcribbonstatusbarpanecmfcribbonstatusbarpane"></a><a name="cmfcribbonstatusbarpane"></a> CMFCRibbonStatusBarPane:: CMFCRibbonStatusBarPane

Создайте объект панели в строке состояния.

```
CMFCRibbonStatusBarPane(
    UINT nCmdID,
    LPCTSTR lpszText,
    BOOL bIsStatic=FALSE,
    HICON hIcon=NULL,
    LPCTSTR lpszAlmostLargeText=NULL);

CMFCRibbonStatusBarPane(
    UINT nCmdID,
    LPCTSTR lpszText,
    HBITMAP hBmpAnimationList,
    int cxAnimation=16,
    COLORREF clrTrnsp=RGB(192,192 1,192) 1,
    HICON hIcon=NULL,
    BOOL bIsStatic=FALSE);

CMFCRibbonStatusBarPane(
    UINT nCmdID,
    LPCTSTR lpszText,
    UINT uiAnimationListResID,
    int cxAnimation=16,
    COLORREF clrTrnsp=RGB(192, 192 1, 192) 1,
    HICON hIcon=NULL,
    BOOL bIsStatic=FALSE);
```

### <a name="parameters"></a>Параметры

*нкмдид*<br/>
окне Указывает идентификатор команды для панели.

*lpszText*<br/>
окне Задает текстовую строку, отображаемую на панели.

*бисстатик*<br/>
окне Если значение — TRUE, область состояния нельзя выделить или выбрать, щелкнув ее.

*hIcon*<br/>
окне Задает маркер для значка, отображаемого на панели.

*лпсзалмостларжетекст*<br/>
окне Указывает длинную текстовую строку, которая может отображаться на панели.

*хбмпаниматионлист*<br/>
окне Задает маркер для списка изображений, используемый для анимации.

*кксаниматион*<br/>
окне Задает ширину (в пикселях) значка в списке изображений, который используется для анимации.

*клртрнсп*<br/>
окне Задает прозрачный цвет изображений в списке изображений, используемых для анимации.

*уианиматионлистресид*<br/>
окне Указывает идентификатор ресурса для списка изображений, используемого для анимации.

## <a name="cmfcribbonstatusbarpanegetalmostlargetext"></a><a name="getalmostlargetext"></a> CMFCRibbonStatusBarPane:: Жеталмостларжетекст

Возвращает самую длинную текстовую строку, которую может отобразить панель строки состояния.

```
LPCTSTR GetAlmostLargeText() const;
```

### <a name="return-value"></a>Возвращаемое значение

Длинная текстовая строка, которую может отобразить панель строки состояния.

## <a name="cmfcribbonstatusbarpanegettextalign"></a><a name="gettextalign"></a> CMFCRibbonStatusBarPane:: Жеттексталигн

Возвращает текущее значение выравнивания текста метки на панели строки состояния.

```
int GetTextAlign() const;
```

### <a name="return-value"></a>Возвращаемое значение

Текущее выравнивание текста, которое может быть одним из следующих:

- TA_LEFT

- TA_CENTER

- TA_RIGHT.

## <a name="cmfcribbonstatusbarpaneisanimation"></a><a name="isanimation"></a> CMFCRibbonStatusBarPane:: Animation

Определяет, выполняется ли анимация.

```
BOOL IsAnimation() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если анимация выполняется; В противном случае — значение FALSE.

## <a name="cmfcribbonstatusbarpaneisextended"></a><a name="isextended"></a> CMFCRibbonStatusBarPane:: Extended

Определите, находится ли панель в расширенной области строки состояния ленты.

```
BOOL IsExtended() const;
```

### <a name="return-value"></a>Возвращаемое значение

TRUE, если область находится в расширенной области строки состояния. В противном случае — значение FALSE.

## <a name="cmfcribbonstatusbarpaneondrawborder"></a><a name="ondrawborder"></a> CMFCRibbonStatusBarPane:: Ондравбордер

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual void OnDrawBorder(CDC*);
```

### <a name="parameters"></a>Параметры

окне *&#42;CDC*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbarpaneonfillbackground"></a><a name="onfillbackground"></a> CMFCRibbonStatusBarPane:: Онфиллбаккграунд

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual COLORREF OnFillBackground(CDC* pDC);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbarpaneonfinishanimation"></a><a name="onfinishanimation"></a> CMFCRibbonStatusBarPane:: Онфинишаниматион

Платформа вызывает этот метод при завершении анимации, назначенной панели.

```
virtual void OnFinishAnimation();
```

### <a name="remarks"></a>Комментарии

`StopAnimation` вызывает `OnFinishAnimation` метод, который можно использовать для очистки данных при окончании анимации.

## <a name="cmfcribbonstatusbarpanesetalmostlargetext"></a><a name="setalmostlargetext"></a> CMFCRibbonStatusBarPane:: Сеталмостларжетекст

Определите самый длинный текст, который может отображаться на панели строка состояния без усечения.

```cpp
void SetAlmostLargeText(LPCTSTR lpszAlmostLargeText);
```

### <a name="parameters"></a>Параметры

*лпсзалмостларжетекст*<br/>
окне Указывает длинную строку, которая может быть отображена на панели строка состояния без усечения.

### <a name="remarks"></a>Комментарии

Библиотека вычисляет размер текста, который *лпсзалмостларжетекст* указывает, и соответствующим образом изменяет размеры панели. Текст будет обрезан, если он по-прежнему не умещается на панели.

## <a name="cmfcribbonstatusbarpanesetanimationlist"></a><a name="setanimationlist"></a> CMFCRibbonStatusBarPane:: Сетаниматионлист

Присоединяет к панели строки состояния список изображений, который можно использовать для анимации.

```cpp
void SetAnimationList(
    HBITMAP hBmpAnimationList,
    int cxAnimation=16,
    COLORREF clrTransp=RGB(192, 192 1, 192) 1);

BOOL SetAnimationList(
    UINT uiAnimationListResID,
    int cxAnimation=16,
    COLORREF clrTransp=RGB(192, 192 1, 192) 1);
```

### <a name="parameters"></a>Параметры

*хбмпаниматионлист*<br/>
окне Задает маркер для списка изображений.

*кксаниматион*<br/>
окне Задает ширину (в пикселях) кадра в списке изображений.

*clrTransp*<br/>
окне Задает прозрачный цвет для списка изображений.

*уианиматионлистресид*<br/>
окне Указывает идентификатор ресурса для списка изображений.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если список изображений успешно присоединен к панели строки состояния; В противном случае — значение FALSE.

## <a name="cmfcribbonstatusbarpanesettextalign"></a><a name="settextalign"></a> CMFCRibbonStatusBarPane:: Сеттексталигн

Задает выравнивание текста метки на панели строки состояния.

```cpp
void SetTextAlign(int nAlign);
```

### <a name="parameters"></a>Параметры

*налигн*<br/>
окне Задает выравнивание текста.

### <a name="remarks"></a>Комментарии

*налигн* может иметь одно из следующих значений:

- TA_LEFT: выравнивание по левому краю

- TA_CENTER: выравнивание по центру

- TA_RIGHT: выравнивание по правому краю

## <a name="cmfcribbonstatusbarpanestartanimation"></a><a name="startanimation"></a> CMFCRibbonStatusBarPane:: Стартаниматион

Запускает анимацию, назначенную панели.

```cpp
void StartAnimation(
    UINT nFrameDelay=500,
    UINT nDuration=-1);
```

### <a name="parameters"></a>Параметры

*нфрамеделай*<br/>
окне Указывает частоту кадров анимации в миллисекундах.

*ндуратион*<br/>
окне Указывает продолжительность воспроизведения анимации в миллисекундах. Для бесконечного цикла используйте параметр-1.

### <a name="remarks"></a>Комментарии

Необходимо указать маркер для списка изображений перед вызовом с `StartAnimation` помощью `SetAnimationList` .

## <a name="cmfcribbonstatusbarpanestopanimation"></a><a name="stopanimation"></a> CMFCRibbonStatusBarPane:: Стопаниматион

Останавливает анимацию, назначенную панели строка состояния.

```cpp
void StopAnimation();
```

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)<br/>
[Класс Кмфкриббонстатусбар](../../mfc/reference/cmfcribbonstatusbar-class.md)
