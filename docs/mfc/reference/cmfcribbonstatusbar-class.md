---
description: 'Дополнительные сведения о: Кмфкриббонстатусбар Class'
title: Класс Кмфкриббонстатусбар
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonStatusBar
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::AddDynamicElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::AddElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::AddExtendedElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::AddSeparator
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::Create
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::CreateEx
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::FindByID
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::FindElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetCount
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetExCount
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetExElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetExtendedArea
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::GetSpace
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::IsBottomFrame
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::IsExtendedElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::IsInformationMode
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::RecalcLayout
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::RemoveAll
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::RemoveElement
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::SetInformation
- AFXRIBBONSTATUSBAR/CMFCRibbonStatusBar::OnDrawInformation
helpviewer_keywords:
- CMFCRibbonStatusBar [MFC], AddDynamicElement
- CMFCRibbonStatusBar [MFC], AddElement
- CMFCRibbonStatusBar [MFC], AddExtendedElement
- CMFCRibbonStatusBar [MFC], AddSeparator
- CMFCRibbonStatusBar [MFC], Create
- CMFCRibbonStatusBar [MFC], CreateEx
- CMFCRibbonStatusBar [MFC], FindByID
- CMFCRibbonStatusBar [MFC], FindElement
- CMFCRibbonStatusBar [MFC], GetCount
- CMFCRibbonStatusBar [MFC], GetElement
- CMFCRibbonStatusBar [MFC], GetExCount
- CMFCRibbonStatusBar [MFC], GetExElement
- CMFCRibbonStatusBar [MFC], GetExtendedArea
- CMFCRibbonStatusBar [MFC], GetSpace
- CMFCRibbonStatusBar [MFC], IsBottomFrame
- CMFCRibbonStatusBar [MFC], IsExtendedElement
- CMFCRibbonStatusBar [MFC], IsInformationMode
- CMFCRibbonStatusBar [MFC], RecalcLayout
- CMFCRibbonStatusBar [MFC], RemoveAll
- CMFCRibbonStatusBar [MFC], RemoveElement
- CMFCRibbonStatusBar [MFC], SetInformation
- CMFCRibbonStatusBar [MFC], OnDrawInformation
ms.assetid: 921eb57f-3b40-49fa-a38c-3f2fb6dc2893
ms.openlocfilehash: 01436d535b410fd4a6c70f52760908e3547b7af8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97265003"
---
# <a name="cmfcribbonstatusbar-class"></a>Класс Кмфкриббонстатусбар

`CMFCRibbonStatusBar`Класс реализует элемент управления "строка состояния", который может отображать элементы ленты.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonStatusBar : public CMFCRibbonBar
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонстатусбар:: Адддинамицелемент](#adddynamicelement)|Добавляет динамический элемент в строку состояния ленты.|
|[Кмфкриббонстатусбар:: Адделемент](#addelement)|Добавляет новый элемент ленты в строку состояния ленты.|
|[Кмфкриббонстатусбар:: Аддекстендеделемент](#addextendedelement)|Добавляет элемент ленты в расширенную область строки состояния ленты.|
|[Кмфкриббонстатусбар:: Аддсепаратор](#addseparator)|Добавляет разделитель в строку состояния ленты.|
|[Кмфкриббонстатусбар:: Create](#create)|Создает строку состояния ленты.|
|[Кмфкриббонстатусбар:: Креатикс](#createex)|Создает строку состояния ленты с расширенным стилем.|
|[Кмфкриббонстатусбар:: Финдбид](#findbyid)||
|[Кмфкриббонстатусбар:: Финделемент](#findelement)|Возвращает указатель на элемент с указанным ИДЕНТИФИКАТОРом команды.|
|[Кмфкриббонстатусбар:: NOCOUNT](#getcount)|Возвращает количество элементов, расположенных в основной области строки состояния ленты.|
|[Кмфкриббонстатусбар:: элемент](#getelement)|Возвращает указатель на элемент, расположенный по указанному индексу.|
|[Кмфкриббонстатусбар:: Жетекскаунт](#getexcount)|Возвращает количество элементов, расположенных в расширенной области строки состояния ленты.|
|[Кмфкриббонстатусбар:: Жетекселемент](#getexelement)|Возвращает указатель на элемент, расположенный по заданному индексу в расширенной области строки состояния ленты.|
|[Кмфкриббонстатусбар:: Жетекстендедареа](#getextendedarea)||
|[Кмфкриббонстатусбар::-пробел](#getspace)||
|[Кмфкриббонстатусбар:: Исботтомфраме](#isbottomframe)||
|[Кмфкриббонстатусбар:: Исекстендеделемент](#isextendedelement)||
|[Кмфкриббонстатусбар:: Исинформатионмоде](#isinformationmode)|Определяет, включен ли режим информации для строки состояния ленты.|
|[Кмфкриббонстатусбар:: RecalcLayout](#recalclayout)|(Переопределяет [CMFCRibbonBar:: RecalcLayout](../../mfc/reference/cmfcribbonbar-class.md#recalclayout).)|
|[Кмфкриббонстатусбар:: RemoveAll](#removeall)|Удаляет все элементы из строки состояния ленты.|
|[Кмфкриббонстатусбар:: Ремовилемент](#removeelement)|Удаляет элемент с указанным ИДЕНТИФИКАТОРом команды из строки состояния ленты.|
|[Кмфкриббонстатусбар:: Сетинформатион](#setinformation)|Включает или отключает режим информации для строки состояния ленты.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кмфкриббонстатусбар:: Ондравинформатион](#ondrawinformation)|Отображает информационную строку, которая отображается в строке состояния ленты, если включен режим информации.|

## <a name="remarks"></a>Комментарии

Пользователи могут изменять видимость элементов ленты в строке состояния ленты, используя встроенное контекстное меню для строки состояния ленты. Элементы можно добавлять или удалять динамически.

Строка состояния ленты имеет две области: Главная и расширенная область. Расширенная область отображается в правой части строки состояния ленты и отображается в цвете, отличном от цвета основной области.

Как правило, в основной области строки состояния отображаются уведомления о состоянии, а в расширенной области — элементы управления представления. Расширенная область остается видимой до тех пор, пока пользователь изменяет размер строки состояния ленты.

## <a name="example"></a>Пример

В приведенном ниже примере демонстрируется использование различных методов класса `CMFCRibbonStatusBar` . В примере показано, как добавить новый элемент ленты в строку состояния ленты, добавить элемент Ribbon в расширенную область строки состояния ленты, добавить разделитель и включить обычный режим для строки состояния ленты.

[!code-cpp[NVC_MFC_RibbonApp#15](../../mfc/reference/codesnippet/cpp/cmfcribbonstatusbar-class_1.cpp)]
[!code-cpp[NVC_MFC_RibbonApp#16](../../mfc/reference/codesnippet/cpp/cmfcribbonstatusbar-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md)

[CMFCRibbonStatusBar](../../mfc/reference/cmfcribbonstatusbar-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонстатусбар. h

## <a name="cmfcribbonstatusbaradddynamicelement"></a><a name="adddynamicelement"></a> Кмфкриббонстатусбар:: Адддинамицелемент

Добавляет динамический элемент в строку состояния ленты.

```cpp
void AddDynamicElement(CMFCRibbonBaseElement* pElement);
```

### <a name="parameters"></a>Параметры

*пелемент*<br/>
окне Указатель на динамический элемент.

### <a name="remarks"></a>Комментарии

В отличие от обычных элементов, динамические элементы не настраиваются, и меню Настройка в строке состояния не отображает их.

## <a name="cmfcribbonstatusbaraddelement"></a><a name="addelement"></a> Кмфкриббонстатусбар:: Адделемент

Добавляет новый элемент ленты в строку состояния ленты.

```cpp
void AddElement(
    CMFCRibbonBaseElement* pElement,
    LPCTSTR lpszLabel,
    BOOL bIsVisible=TRUE);
```

### <a name="parameters"></a>Параметры

*пелемент*<br/>
окне Указатель на добавленный элемент.

*лпсзлабел*<br/>
окне Текстовая метка элемента.

*бисвисибле*<br/>
окне Значение TRUE, если необходимо добавить элемент как видимый, и FALSE, если требуется добавить элемент как скрытый.

## <a name="cmfcribbonstatusbaraddextendedelement"></a><a name="addextendedelement"></a> Кмфкриббонстатусбар:: Аддекстендеделемент

Добавляет элемент ленты в расширенную область строки состояния ленты.

```cpp
void AddExtendedElement(
    CMFCRibbonBaseElement* pElement,
    LPCTSTR lpszLabel,
    BOOL bIsVisible=TRUE);
```

### <a name="parameters"></a>Параметры

*пелемент*<br/>
окне Указатель на добавленный элемент.

*лпсзлабел*<br/>
окне Текстовая метка элемента.

*бисвисибле*<br/>
окне Значение TRUE, если необходимо добавить элемент как видимый, и FALSE, если требуется добавить элемент как скрытый.

### <a name="remarks"></a>Комментарии

Расширенная область находится в правой части элемента управления состоянием строки.

## <a name="cmfcribbonstatusbaraddseparator"></a><a name="addseparator"></a> Кмфкриббонстатусбар:: Аддсепаратор

Добавляет разделитель в строку состояния ленты.

```cpp
void AddSeparator();
```

### <a name="remarks"></a>Комментарии

Платформа добавляет разделитель после метода [кмфкриббонстатусбар:: адделемент](#addelement). Вставляет последний элемент.

## <a name="cmfcribbonstatusbarcreate"></a><a name="create"></a> Кмфкриббонстатусбар:: Create

Создает строку состояния ленты.

```
BOOL Create(
    CWnd* pParentWnd,
    DWORD dwStyle=WS_CHILD|WS_VISIBLE|CBRS_BOTTOM,
    UINT nID=AFX_IDW_STATUS_BAR);
```

### <a name="parameters"></a>Параметры

*ппарентвнд*<br/>
окне Указатель на родительское окно.

*двстиле*<br/>
окне Логическое или сочетание стилей элементов управления.

*nID*<br/>
окне Идентификатор элемента управления строки состояния.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если строка состояния создана успешно; в противном случае — значение FALSE.

## <a name="cmfcribbonstatusbarcreateex"></a><a name="createex"></a> Кмфкриббонстатусбар:: Креатикс

Создает строку состояния ленты с расширенным стилем.

```
BOOL CreateEx(
    CWnd* pParentWnd,
    DWORD dwCtrlStyle=0,
    DWORD dwStyle=WS_CHILD|WS_VISIBLE|CBRS_BOTTOM,
    UINT nID=AFX_IDW_STATUS_BAR);
```

### <a name="parameters"></a>Параметры

*ппарентвнд*<br/>
Указатель на родительское окно.

*двктрлстиле*<br/>
Логическое или сочетание дополнительных стилей для создания объекта строки состояния.

*двстиле*<br/>
Стиль элемента управления строки состояния.

*nID*<br/>
Идентификатор элемента управления строки состояния.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если строка состояния создана успешно; в противном случае — значение FALSE.

## <a name="cmfcribbonstatusbarfindbyid"></a><a name="findbyid"></a> Кмфкриббонстатусбар:: Финдбид

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
CMFCRibbonBaseElement* FindByID(UINT uiCmdID, BOOL = TRUE);
```

### <a name="parameters"></a>Параметры

окне *уикмдид*<br/>
окне *Bool (логическое* )<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbarfindelement"></a><a name="findelement"></a> Кмфкриббонстатусбар:: Финделемент

Возвращает указатель на элемент с указанным ИДЕНТИФИКАТОРом команды.

```
CMFCRibbonBaseElement* FindElement(UINT uiID);
```

### <a name="parameters"></a>Параметры

*uiID*<br/>
окне Идентификатор элемента.

### <a name="return-value"></a>Возвращаемое значение

Указатель на элемент с указанным ИДЕНТИФИКАТОРом команды. Значение NULL, если такого элемента нет.

## <a name="cmfcribbonstatusbargetcount"></a><a name="getcount"></a> Кмфкриббонстатусбар:: NOCOUNT

Возвращает количество элементов, расположенных в основной области строки состояния ленты.

```
int GetCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Количество элементов, расположенных в основной области строки состояния ленты.

## <a name="cmfcribbonstatusbargetelement"></a><a name="getelement"></a> Кмфкриббонстатусбар:: элемент

Возвращает указатель на элемент, расположенный по указанному индексу.

```
CMFCRibbonBaseElement* GetElement(int nIndex);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
окне Задает отсчитываемый от нуля индекс элемента, который находится в основной области элемента управления "строка состояния".

### <a name="return-value"></a>Возвращаемое значение

Указатель на элемент, расположенный по указанному индексу. Значение NULL, если индекс отрицательный или превышает число элементов в строке состояния.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbargetexcount"></a><a name="getexcount"></a> Кмфкриббонстатусбар:: Жетекскаунт

Возвращает количество элементов, расположенных в расширенной области строки состояния ленты.

```
int GetExCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Количество элементов, расположенных в расширенной области строки состояния ленты.

## <a name="cmfcribbonstatusbargetexelement"></a><a name="getexelement"></a> Кмфкриббонстатусбар:: Жетекселемент

Возвращает указатель на элемент, расположенный по заданному индексу в расширенной области строки состояния ленты. Расширенная область находится в правой части элемента управления состоянием строки.

```
CMFCRibbonBaseElement* GetExElement(int nIndex);
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
окне Задает отсчитываемый от нуля индекс элемента, который находится в расширенной области элемента управления "строка состояния".

### <a name="return-value"></a>Возвращаемое значение

Указатель на элемент, расположенный по заданному индексу в расширенной области строки состояния ленты. Значение NULL, если *ниндекс* является отрицательным или превышает число элементов в расширенной области строки состояния ленты.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbargetextendedarea"></a><a name="getextendedarea"></a> Кмфкриббонстатусбар:: Жетекстендедареа

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual BOOL GetExtendedArea(CRect& rect) const;
```

### <a name="parameters"></a>Параметры

[in] *rect*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbargetspace"></a><a name="getspace"></a> Кмфкриббонстатусбар::-пробел

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
int GetSpace() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbarisbottomframe"></a><a name="isbottomframe"></a> Кмфкриббонстатусбар:: Исботтомфраме

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
BOOL IsBottomFrame() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbarisextendedelement"></a><a name="isextendedelement"></a> Кмфкриббонстатусбар:: Исекстендеделемент

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
BOOL IsExtendedElement(CMFCRibbonBaseElement* pElement) const;
```

### <a name="parameters"></a>Параметры

окне *пелемент*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbarisinformationmode"></a><a name="isinformationmode"></a> Кмфкриббонстатусбар:: Исинформатионмоде

Определяет, включен ли режим информации для строки состояния ленты.

```
BOOL IsInformationMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если строка состояния может работать в информационном режиме; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

В режиме информации строка состояния скрывает все обычные панели и отображает строку сообщения.

## <a name="cmfcribbonstatusbarondrawinformation"></a><a name="ondrawinformation"></a> Кмфкриббонстатусбар:: Ондравинформатион

Отображает строку, которая отображается в строке состояния ленты при включенном информационном режиме.

```
virtual void OnDrawInformation(
    CDC* pDC,
    CString& strInfo,
    CRect rectInfo);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*стринфо*<br/>
окне Информационная строка.

*ректинфо*<br/>
окне Ограничивающий прямоугольник.

### <a name="remarks"></a>Комментарии

Переопределите этот метод в производном классе, если необходимо настроить внешний вид информационной строки в строке состояния. Используйте метод [кмфкриббонстатусбар:: сетинформатион](#setinformation) , чтобы перевести строку состояния в режим информации. В этом режиме строка состояния скрывает все области и отображает информационную строку, указанную параметром *стринфо*.

## <a name="cmfcribbonstatusbarrecalclayout"></a><a name="recalclayout"></a> Кмфкриббонстатусбар:: RecalcLayout

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual void RecalcLayout();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonstatusbarremoveall"></a><a name="removeall"></a> Кмфкриббонстатусбар:: RemoveAll

Удаляет все элементы из строки состояния ленты.

```cpp
void RemoveAll();
```

## <a name="cmfcribbonstatusbarremoveelement"></a><a name="removeelement"></a> Кмфкриббонстатусбар:: Ремовилемент

Удаляет элемент с указанным ИДЕНТИФИКАТОРом команды из строки состояния ленты.

```
BOOL RemoveElement(UINT uiID);
```

### <a name="parameters"></a>Параметры

*uiID*<br/>
окне Идентификатор элемента, который необходимо удалить из строки состояния.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если удаляется элемент с указанным *уиид* . В противном случае — значение FALSE.

## <a name="cmfcribbonstatusbarsetinformation"></a><a name="setinformation"></a> Кмфкриббонстатусбар:: Сетинформатион

Включает или отключает режим информации для строки состояния ленты.

```cpp
void SetInformation(LPCTSTR lpszInfo);
```

### <a name="parameters"></a>Параметры

*лпсзинфо*<br/>
окне Информационная строка.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы перевести строку состояния в информационный режим. В этом режиме строка состояния скрывает все области и отображает информационную строку, указанную параметром *лпсзинфо*.

Если Лпсзинфо имеет значение NULL, строка состояния возвращается в обычный режим.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md)<br/>
[Класс метод CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)<br/>
[Класс CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md)
