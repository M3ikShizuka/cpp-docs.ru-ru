---
description: 'Дополнительные сведения о: CMFCDesktopAlertWnd Class'
title: CMFCDesktopAlertWnd Class
ms.date: 10/18/2018
f1_keywords:
- CMFCDesktopAlertWnd
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::Create
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::GetAnimationSpeed
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::GetAnimationType
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::GetAutoCloseTime
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::GetCaptionHeight
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::GetDialogSize
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::GetLastPos
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::GetTransparency
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::HasSmallCaption
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::OnBeforeShow
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::OnClickLinkButton
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::OnCommand
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::OnDraw
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::ProcessCommand
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::SetAnimationSpeed
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::SetAnimationType
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::SetAutoCloseTime
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::SetSmallCaption
- AFXDESKTOPALERTWND/CMFCDesktopAlertWnd::SetTransparency
helpviewer_keywords:
- CMFCDesktopAlertWnd [MFC], Create
- CMFCDesktopAlertWnd [MFC], GetAnimationSpeed
- CMFCDesktopAlertWnd [MFC], GetAnimationType
- CMFCDesktopAlertWnd [MFC], GetAutoCloseTime
- CMFCDesktopAlertWnd [MFC], GetCaptionHeight
- CMFCDesktopAlertWnd [MFC], GetDialogSize
- CMFCDesktopAlertWnd [MFC], GetLastPos
- CMFCDesktopAlertWnd [MFC], GetTransparency
- CMFCDesktopAlertWnd [MFC], HasSmallCaption
- CMFCDesktopAlertWnd [MFC], OnBeforeShow
- CMFCDesktopAlertWnd [MFC], OnClickLinkButton
- CMFCDesktopAlertWnd [MFC], OnCommand
- CMFCDesktopAlertWnd [MFC], OnDraw
- CMFCDesktopAlertWnd [MFC], ProcessCommand
- CMFCDesktopAlertWnd [MFC], SetAnimationSpeed
- CMFCDesktopAlertWnd [MFC], SetAnimationType
- CMFCDesktopAlertWnd [MFC], SetAutoCloseTime
- CMFCDesktopAlertWnd [MFC], SetSmallCaption
- CMFCDesktopAlertWnd [MFC], SetTransparency
ms.assetid: 73a2dd7b-ea84-4ae2-9830-7cf6e8dd2425
ms.openlocfilehash: 45b75bdbd24a88a7eacff124bb07ac81e7703c31
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330089"
---
# <a name="cmfcdesktopalertwnd-class"></a>CMFCDesktopAlertWnd Class

`CMFCDesktopAlertWnd`Класс реализует функциональные возможности немодального диалогового окна, которое отображается на экране для информирования пользователя о событии.

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMFCDesktopAlertWnd : public CWnd
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCDesktopAlertWnd:: Create](#create)|Создает и инициализирует окно оповещения рабочего стола.|
|[CMFCDesktopAlertWnd:: Жетаниматионспид](#getanimationspeed)|Возвращает скорость анимации.|
|[CMFCDesktopAlertWnd:: Жетаниматионтипе](#getanimationtype)|Возвращает тип анимации.|
|[CMFCDesktopAlertWnd:: Жетаутоклосетиме](#getautoclosetime)|Возвращает время ожидания автоматического закрытия.|
|[CMFCDesktopAlertWnd:: Жеткаптионхеигхт](#getcaptionheight)|Возвращает высоту заголовка.|
|[CMFCDesktopAlertWnd:: Жетдиалогсизе](#getdialogsize)||
|[CMFCDesktopAlertWnd:: Жетластпос](#getlastpos)|Возвращает последнюю допустимую точку окна оповещения рабочего стола на экране.|
|[CMFCDesktopAlertWnd:: "прозрачность"](#gettransparency)|Возвращает уровень прозрачности.|
|[CMFCDesktopAlertWnd:: Хассмаллкаптион](#hassmallcaption)|Определяет, отображается ли окно оповещения рабочего стола с небольшим заголовком.|
|[CMFCDesktopAlertWnd:: Онбефорешов](#onbeforeshow)||
|[CMFCDesktopAlertWnd:: Онкликклинкбуттон](#onclicklinkbutton)|Вызывается структурой при нажатии пользователем кнопки "ссылка" в меню "предупреждение" рабочего стола.|
|[CMFCDesktopAlertWnd:: OnCommand](#oncommand)|Платформа вызывает эту функцию-член, когда пользователь выбирает элемент из меню, когда дочерний элемент управления отправляет сообщение уведомления или при преобразовании нажатия клавиши быстрого вызова. (Переопределяет [CWnd:: OnCommand](../../mfc/reference/cwnd-class.md#oncommand).)|
|[CMFCDesktopAlertWnd:: OnDraw](#ondraw)||
|[CMFCDesktopAlertWnd::P Роцесскомманд](#processcommand)||
|[CMFCDesktopAlertWnd:: Сетаниматионспид](#setanimationspeed)|Задает новую скорость анимации.|
|[CMFCDesktopAlertWnd:: Сетаниматионтипе](#setanimationtype)|Задает тип анимации.|
|[CMFCDesktopAlertWnd:: Сетаутоклосетиме](#setautoclosetime)|Задает время ожидания автоматического закрытия.|
|[CMFCDesktopAlertWnd:: Сетсмаллкаптион](#setsmallcaption)|Переключение между мелкими и обычными заголовками.|
|[CMFCDesktopAlertWnd:: Сеттранспаренци](#settransparency)|Задает уровень прозрачности.|

## <a name="remarks"></a>Комментарии

Окно оповещений на рабочем столе может быть прозрачным, оно может отображаться с эффектами анимации и исчезает (после определенной задержки или когда пользователь закрывает его, нажав кнопку Закрыть).

Окно оповещения на рабочем столе также может содержать диалоговое окно по умолчанию, которое, в свою очередь, содержит значок, текст сообщения (метка) и ссылку. Кроме того, окно оповещения на рабочем столе может содержать пользовательское диалоговое окно из ресурсов приложения.

Окно предупреждения создается на рабочем столе в два этапа. Сначала вызовите конструктор для создания `CMFCDesktopAlertWnd` объекта. Во вторых, вызовите функцию члена [CMFCDesktopAlertWnd:: Create](#create) , чтобы создать окно и присоединить его к `CMFCDesktopAlertWnd` объекту.

`CMFCDesktopAlertWnd`Объект создает специальное дочернее диалоговое окно, которое заполняет клиентскую область окна оповещения рабочего стола. Диалоговое окно владеет всеми элементами управления, расположенными на нем.

Чтобы отобразить пользовательское диалоговое окно во всплывающем окне, выполните следующие действия.

1. Создайте производный класс от класса `CMFCDesktopAlertDialog`.

1. Создайте дочерний шаблон диалогового окна в ресурсах.

1. Вызовите метод [CMFCDesktopAlertWnd:: Create](#create) , используя идентификатор ресурса шаблона диалогового окна, и указатель на сведения о классе среды выполнения производного класса.

1. Запрограммировать настраиваемое диалоговое окно для поддержки всех уведомлений, поступающих от размещенных элементов управления, или программировать размещенные элементы управления для непосредственной работы с этими уведомлениями.

Используйте следующие функции для управления поведением окна оповещения рабочего стола:

- Задайте тип анимации, вызвав [CMFCDesktopAlertWnd:: сетаниматионтипе](#setanimationtype). Допустимые параметры: unfold, скольжение и выцветание.

- Задайте скорость кадров анимации, вызвав [CMFCDesktopAlertWnd:: сетаниматионспид](#setanimationspeed).

- Задайте уровень прозрачности, вызвав [CMFCDesktopAlertWnd:: сеттранспаренци](#settransparency).

- Измените размер заголовка на малый, вызвав [CMFCDesktopAlertWnd:: сетсмаллкаптион](#setsmallcaption). Маленький заголовок — 7 пикселей в высоком.

## <a name="example"></a>Пример

В следующем примере показано, как использовать различные методы в `CMFCDesktopAlertWnd` классе для настройки `CMFCDesktopAlertWnd` объекта. В этом примере показано, как задать тип анимации, задать прозрачность всплывающего окна, указать, что окно предупреждения отображает маленький заголовок, и задать время, по истечении которого окно предупреждения автоматически закроется. В примере также показано, как создать и инициализировать окно оповещения рабочего стола. Этот фрагмент кода является частью [демонстрационного примера оповещения Desktop](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_DesktopAlertDemo#1](../../mfc/reference/codesnippet/cpp/cmfcdesktopalertwnd-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CMFCDesktopAlertWnd](../../mfc/reference/cmfcdesktopalertwnd-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксдесктопалертвнд. h

## <a name="cmfcdesktopalertwndcreate"></a><a name="create"></a> CMFCDesktopAlertWnd:: Create

Создает и инициализирует окно оповещения рабочего стола.

```
virtual BOOL Create(
    CWnd* pWndOwner,
    UINT uiDlgResID,
    HMENU hMenu = NULL,
    CPoint ptPos = CPoint(-1,-1),
    CRuntimeClass* pRTIDlgBar = RUNTIME_CLASS(CMFCDesktopAlertDialog));

virtual BOOL Create(
    CWnd* pWndOwner,
    CMFCDesktopAlertWndInfo& params,
    HMENU hMenu = NULL,
    CPoint ptPos = CPoint(-1,-1));
```

### <a name="parameters"></a>Параметры

*пвндовнер*<br/>
[вход, выход] Указывает владельца окна предупреждения. Затем этот владелец будет получать все уведомления для окна оповещения рабочего стола. Это значение не может быть равно NULL.

*уидлгресид*<br/>
окне Указывает идентификатор ресурса окна предупреждения.

*hMenu*<br/>
окне Задает меню, которое отображается, когда пользователь нажимает кнопку меню. Если значение равно NULL, кнопка меню не отображается.

*птпос*<br/>
окне Указывает начальную позицию, в которой отображается окно предупреждения, с помощью экранных координат. Если этот параметр имеет значение (-1,-1), окно предупреждения отображается в правом нижнем углу экрана.

*пртидлгбар*<br/>
окне Сведения о классе среды выполнения для пользовательского класса диалогового окна, охватывающего клиентскую область окна предупреждения.

*params*<br/>
окне Указывает параметры, используемые для создания окна предупреждения.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если окно предупреждения успешно создано; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы создать окно предупреждения. В клиентской области окна предупреждения содержится дочернее диалоговое окно, в котором размещены все элементы управления, отображаемые для пользователя.

Перегрузка первого метода создает окно предупреждения, содержащее дочернее диалоговое окно, которое загружается из ресурсов приложения. В первой перегрузке метода также можно указать сведения о классе среды выполнения для пользовательского класса диалогового окна.

Вторая перегрузка метода создает окно предупреждения, содержащее элементы управления по умолчанию. Можно указать, какие элементы управления должны отображаться, изменив [класс кмфкдесктопалертвндинфо](../../mfc/reference/cmfcdesktopalertwndinfo-class.md).

## <a name="cmfcdesktopalertwndgetanimationspeed"></a><a name="getanimationspeed"></a> CMFCDesktopAlertWnd:: Жетаниматионспид

Возвращает скорость анимации.

```
UINT GetAnimationSpeed() const;
```

### <a name="return-value"></a>Возвращаемое значение

Скорость анимации окна предупреждения в миллисекундах.

### <a name="remarks"></a>Комментарии

Скорость анимации показывает, как быстро открывается и закрывается окно оповещений.

## <a name="cmfcdesktopalertwndgetanimationtype"></a><a name="getanimationtype"></a> CMFCDesktopAlertWnd:: Жетаниматионтипе

Возвращает тип анимации.

```
CMFCPopupMenu::ANIMATION_TYPE GetAnimationType();
```

### <a name="return-value"></a>Возвращаемое значение

Один из следующих типов анимации:

- NO_ANIMATION

- UNFOLD

- СЛАЙД

- АНИМАЦИИ

- SYSTEM_DEFAULT_ANIMATION

## <a name="cmfcdesktopalertwndgetautoclosetime"></a><a name="getautoclosetime"></a> CMFCDesktopAlertWnd:: Жетаутоклосетиме

Возвращает время ожидания автоматического закрытия.

```
int GetAutoCloseTime() const;
```

### <a name="return-value"></a>Возвращаемое значение

Время в миллисекундах, по истечении которого окно предупреждения будет автоматически закрыто.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы определить, сколько времени должно пройти до того, как окно предупреждения будет автоматически закрыто.

## <a name="cmfcdesktopalertwndgetcaptionheight"></a><a name="getcaptionheight"></a> CMFCDesktopAlertWnd:: Жеткаптионхеигхт

Возвращает высоту заголовка.

```
virtual int GetCaptionHeight();
```

### <a name="return-value"></a>Возвращаемое значение

Высота заголовка в пикселях.

### <a name="remarks"></a>Комментарии

Этот метод можно переопределить в производном классе. Реализация по умолчанию: Возвращает значение высоты небольшого заголовка (7 пикселей), если всплывающее окно должно отображать маленький заголовок или значение, полученное от функции Windows API `GetSystemMetrics(SM_CYSMCAPTION)` .

## <a name="cmfcdesktopalertwndgetlastpos"></a><a name="getlastpos"></a> CMFCDesktopAlertWnd:: Жетластпос

Возвращает последнюю точку окна оповещения рабочего стола на экране.

```
CPoint GetLastPos() const;
```

### <a name="return-value"></a>Возвращаемое значение

Точка в экранных координатах.

### <a name="remarks"></a>Комментарии

Этот метод возвращает последнюю допустимую точку окна предупреждения на экране.

## <a name="cmfcdesktopalertwndgettransparency"></a><a name="gettransparency"></a> CMFCDesktopAlertWnd:: "прозрачность"

Возвращает уровень прозрачности.

```
BYTE GetTransparency() const;
```

### <a name="return-value"></a>Возвращаемое значение

Уровень прозрачности от 0 до 255 включительно. Чем больше значение, тем больше непрозрачно окно.

### <a name="remarks"></a>Комментарии

Этот метод используется для получения текущего уровня прозрачности окна предупреждения.

## <a name="cmfcdesktopalertwndhassmallcaption"></a><a name="hassmallcaption"></a> CMFCDesktopAlertWnd:: Хассмаллкаптион

Определяет, имеет ли окно оповещения рабочего стола небольшой заголовок или заголовок обычного размера.

```
BOOL HasSmallCaption() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если всплывающее окно отображается с небольшим заголовком; Значение FALSE, если всплывающее окно отображается с подписью обычного размера.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы определить, имеет ли всплывающее окно небольшой заголовок или заголовок обычного размера. По умолчанию мелкий заголовок имеет значение 7 пикселей. Можно получить высоту заголовка обычного размера, вызвав функцию Windows API `GetSystemMetrics(SM_CYCAPTION)` .

## <a name="cmfcdesktopalertwndonbeforeshow"></a><a name="onbeforeshow"></a> CMFCDesktopAlertWnd:: Онбефорешов

```
virtual BOOL OnBeforeShow(CPoint&);
```

### <a name="parameters"></a>Параметры

окне *CPoint&*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertwndonclicklinkbutton"></a><a name="onclicklinkbutton"></a> CMFCDesktopAlertWnd:: Онкликклинкбуттон

Вызывается структурой при нажатии пользователем кнопки "ссылка" в меню "предупреждение" рабочего стола.

```
virtual BOOL OnClickLinkButton(UINT uiCmdID);
```

### <a name="parameters"></a>Параметры

*уикмдид*<br/>
окне Этот параметр не используется.

### <a name="return-value"></a>Возвращаемое значение

Всегда значение FALSE.

### <a name="remarks"></a>Remarks

Переопределите этот метод в производном классе, если хотите получать уведомления, когда пользователь щелкнет ссылку в окне оповещения.

## <a name="cmfcdesktopalertwndoncommand"></a><a name="oncommand"></a> CMFCDesktopAlertWnd:: OnCommand

```
virtual BOOL OnCommand(
    WPARAM wParam,
    LPARAM lParam);
```

### <a name="parameters"></a>Параметры

окне *wParam*<br/>

окне *lParam*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertwndondraw"></a><a name="ondraw"></a> CMFCDesktopAlertWnd:: OnDraw

```
virtual void OnDraw(CDC* pDC);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertwndprocesscommand"></a><a name="processcommand"></a> CMFCDesktopAlertWnd::P Роцесскомманд

```
BOOL ProcessCommand(HWND hwnd);
```

### <a name="parameters"></a>Параметры

окне *HWND*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertwndsetanimationspeed"></a><a name="setanimationspeed"></a> CMFCDesktopAlertWnd:: Сетаниматионспид

Задает новую скорость анимации.

```cpp
void SetAnimationSpeed(UINT nSpeed);
```

### <a name="parameters"></a>Параметры

*нспид*<br/>
окне Указывает новую скорость анимации в миллисекундах.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы задать скорость анимации для окна предупреждения. Скорость анимации по умолчанию составляет 30 миллисекунд.

## <a name="cmfcdesktopalertwndsetanimationtype"></a><a name="setanimationtype"></a> CMFCDesktopAlertWnd:: Сетаниматионтипе

Задает тип анимации.

```cpp
void SetAnimationType(CMFCPopupMenu::ANIMATION_TYPE type);
```

### <a name="parameters"></a>Параметры

*type*<br/>
окне Указывает тип анимации.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы задать тип анимации. Можно указать одно из следующих значений.

- NO_ANIMATION

- UNFOLD

- СЛАЙД

- АНИМАЦИИ

- SYSTEM_DEFAULT_ANIMATION

## <a name="cmfcdesktopalertwndsetautoclosetime"></a><a name="setautoclosetime"></a> CMFCDesktopAlertWnd:: Сетаутоклосетиме

Задает время ожидания автоматического закрытия.

```cpp
void SetAutoCloseTime(int nTime);
```

### <a name="parameters"></a>Параметры

*Nвремя*<br/>
окне Время в миллисекундах, прошедшее до автоматического закрытия окна предупреждения.

### <a name="remarks"></a>Комментарии

Окно предупреждения автоматически закрывается по истечении указанного времени, если пользователь не взаимодействует с окном.

## <a name="cmfcdesktopalertwndsetsmallcaption"></a><a name="setsmallcaption"></a> CMFCDesktopAlertWnd:: Сетсмаллкаптион

Переключение между небольшими и постоянными заголовками.

```cpp
void SetSmallCaption(BOOL bSmallCaption = TRUE);
```

### <a name="parameters"></a>Параметры

*бсмаллкаптион*<br/>
окне Значение TRUE, чтобы указать, что в окне предупреждения отображается маленький заголовок; в противном случае — значение FALSE, чтобы указать, что в окне предупреждения отображается заголовок обычного размера.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы отобразить заголовок малого или обычного размера. По умолчанию мелкий заголовок имеет значение 7 пикселей. Размер обычного заголовка можно получить, вызвав функцию Windows API `GetSystemMetrics(SM_CYCAPTION)` .

## <a name="cmfcdesktopalertwndsettransparency"></a><a name="settransparency"></a> CMFCDesktopAlertWnd:: Сеттранспаренци

Задает уровень прозрачности всплывающего окна.

```cpp
void SetTransparency(BYTE nTransparency);
```

### <a name="parameters"></a>Параметры

*нтранспаренци*<br/>
окне Задает уровень прозрачности. Это значение должно находиться в диапазоне от 0 до 255 включительно. Чем больше значение, тем больше непрозрачно окно.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы задать уровень прозрачности всплывающего окна.

## <a name="cmfcdesktopalertwndgetdialogsize"></a><a name="getdialogsize"></a> CMFCDesktopAlertWnd:: Жетдиалогсизе

```
virtual CSize GetDialogSize();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкдесктопалертвндинфо](../../mfc/reference/cmfcdesktopalertwndinfo-class.md)<br/>
[Класс Кмфкдесктопалертдиалог](../../mfc/reference/cmfcdesktopalertdialog-class.md)<br/>
[CWnd, класс](../../mfc/reference/cwnd-class.md)
