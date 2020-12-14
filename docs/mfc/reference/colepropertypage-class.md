---
description: 'Дополнительные сведения о: COlePropertyPage Class'
title: Класс COlePropertyPage
ms.date: 11/04/2016
f1_keywords:
- COlePropertyPage
- AFXCTL/COlePropertyPage
- AFXCTL/COlePropertyPage::COlePropertyPage
- AFXCTL/COlePropertyPage::GetControlStatus
- AFXCTL/COlePropertyPage::GetObjectArray
- AFXCTL/COlePropertyPage::GetPageSite
- AFXCTL/COlePropertyPage::OVERWRITEApply
- AFXCTL/COlePropertyPage::IsModified
- AFXCTL/COlePropertyPage::OnEditProperty
- AFXCTL/COlePropertyPage::OnHelp
- AFXCTL/COlePropertyPage::OnInitDialog
- AFXCTL/COlePropertyPage::OnObjectsChanged
- AFXCTL/COlePropertyPage::OnSetPageSite
- AFXCTL/COlePropertyPage::SetControlStatus
- AFXCTL/COlePropertyPage::SetDialogResource
- AFXCTL/COlePropertyPage::SetHelpInfo
- AFXCTL/COlePropertyPage::SetModifiedFlag
- AFXCTL/COlePropertyPage::SetPageName
helpviewer_keywords:
- COlePropertyPage [MFC], COlePropertyPage
- COlePropertyPage [MFC], GetControlStatus
- COlePropertyPage [MFC], GetObjectArray
- COlePropertyPage [MFC], GetPageSite
- COlePropertyPage [MFC], IgnoreApply
- COlePropertyPage [MFC], IsModified
- COlePropertyPage [MFC], OnEditProperty
- COlePropertyPage [MFC], OnHelp
- COlePropertyPage [MFC], OnInitDialog
- COlePropertyPage [MFC], OnObjectsChanged
- COlePropertyPage [MFC], OnSetPageSite
- COlePropertyPage [MFC], SetControlStatus
- COlePropertyPage [MFC], SetDialogResource
- COlePropertyPage [MFC], SetHelpInfo
- COlePropertyPage [MFC], SetModifiedFlag
- COlePropertyPage [MFC], SetPageName
ms.assetid: e9972872-8e6b-4550-905e-d36a274d64dc
ms.openlocfilehash: 56d5696e16a347bab5ed154faf9038c6add446dd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226731"
---
# <a name="colepropertypage-class"></a>Класс COlePropertyPage

Используется для отображения свойств пользовательского элемента управления в графическом интерфейсе подобно диалоговому окну.

## <a name="syntax"></a>Синтаксис

```
class AFX_NOVTABLE COlePropertyPage : public CDialog
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[COlePropertyPage:: COlePropertyPage](#colepropertypage)|Формирует объект `COlePropertyPage`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[COlePropertyPage:: Жетконтролстатус](#getcontrolstatus)|Указывает, изменил ли пользователь значение в элементе управления.|
|[COlePropertyPage:: Жетобжектаррай](#getobjectarray)|Возвращает массив объектов, редактируемых страницей свойств.|
|[COlePropertyPage:: Жетпажесите](#getpagesite)|Возвращает указатель на интерфейс страницы свойств `IPropertyPageSite` .|
|[COlePropertyPage:: Игнореаппли](#ignoreapply)|Определяет, какие элементы управления не включают кнопку "Применить".|
|[COlePropertyPage:: Modified](#ismodified)|Указывает, изменил ли пользователь страницу свойств.|
|[COlePropertyPage:: Онедитпроперти](#oneditproperty)|Вызывается структурой при изменении пользователем свойства.|
|[COlePropertyPage:: OnHelp](#onhelp)|Вызывается платформой при вызове пользователем справки.|
|[COlePropertyPage:: Онинитдиалог](#oninitdialog)|Вызывается структурой при инициализации страницы свойств.|
|[COlePropertyPage:: Онобжектсчанжед](#onobjectschanged)|Вызывается структурой при выборе другого элемента управления OLE с новыми свойствами.|
|[COlePropertyPage:: Онсетпажесите](#onsetpagesite)|Вызывается платформой, когда кадр свойства предоставляет сайт страницы.|
|[COlePropertyPage:: Сетконтролстатус](#setcontrolstatus)|Задает флаг, указывающий, изменил ли пользователь значение в элементе управления.|
|[COlePropertyPage:: Сетдиалогресаурце](#setdialogresource)|Задает ресурс диалога страницы свойств.|
|[COlePropertyPage:: Сеселпинфо](#sethelpinfo)|Задает краткий текст справки для страницы свойств, имя файла справки и контекст справки.|
|[COlePropertyPage:: SetModifiedFlag](#setmodifiedflag)|Задает флаг, указывающий, изменил ли пользователь страницу свойств.|
|[COlePropertyPage:: Сетпаженаме](#setpagename)|Задает имя страницы свойств (заголовок).|

## <a name="remarks"></a>Комментарии

Например, страница свойств может включать элемент управления «поле ввода», позволяющий пользователю просматривать и изменять свойство Caption элемента управления.

Каждое свойство пользовательского или стандартного элемента управления может иметь элемент управления диалогового окна, позволяющий пользователю элемента управления просматривать текущее значение свойства и при необходимости изменять это значение.

Дополнительные сведения об использовании см `COlePropertyPage` . в статье [элементы управления ActiveX: страницы свойств](../../mfc/mfc-activex-controls-property-pages.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

`COlePropertyPage`

## <a name="requirements"></a>Требования

**Заголовок:** afxctl. h

## <a name="colepropertypagecolepropertypage"></a><a name="colepropertypage"></a> COlePropertyPage:: COlePropertyPage

Формирует объект `COlePropertyPage`.

```
COlePropertyPage(
    UINT idDlg,
    UINT idCaption);
```

### <a name="parameters"></a>Параметры

*иддлг*<br/>
Идентификатор ресурса шаблона диалогового окна.

*идкаптион*<br/>
Идентификатор ресурса заголовка страницы свойств.

### <a name="remarks"></a>Комментарии

При реализации подкласса `COlePropertyPage` конструктора Конструктор класса должен использовать `COlePropertyPage` конструктор для указания ресурса шаблона диалогового окна, на котором основана страница свойств, и строкового ресурса, содержащего его заголовок.

## <a name="colepropertypagegetcontrolstatus"></a><a name="getcontrolstatus"></a> COlePropertyPage:: Жетконтролстатус

Определяет, изменил ли пользователь значение элемента управления страницы свойств указанным ИДЕНТИФИКАТОРом ресурса.

```
BOOL GetControlStatus(UINT nID);
```

### <a name="parameters"></a>Параметры

*nID*<br/>
Идентификатор ресурса элемента управления страницы свойств.

### <a name="return-value"></a>Возвращаемое значение

TRUE, если значение элемента управления было изменено; в противном случае — FALSE.

## <a name="colepropertypagegetobjectarray"></a><a name="getobjectarray"></a> COlePropertyPage:: Жетобжектаррай

Возвращает массив объектов, редактируемых страницей свойств.

```
LPDISPATCH* GetObjectArray(ULONG* pnObjects);
```

### <a name="parameters"></a>Параметры

*пнобжектс*<br/>
Указатель на длинное целое число без знака, которое будет принимать количество объектов, редактируемых страницей.

### <a name="return-value"></a>Возвращаемое значение

Указатель на массив `IDispatch` указателей, которые используются для доступа к свойствам каждого элемента управления на странице свойств. Вызывающий объект не должен освобождать эти указатели интерфейсов.

### <a name="remarks"></a>Комментарии

Каждый объект страницы свойств поддерживает массив указателей на `IDispatch` интерфейсы объектов, редактируемых страницей. Эта функция задает для аргумента *пнобжектс* число элементов в этом массиве и возвращает указатель на первый элемент массива.

## <a name="colepropertypagegetpagesite"></a><a name="getpagesite"></a> COlePropertyPage:: Жетпажесите

Возвращает указатель на интерфейс страницы свойств `IPropertyPageSite` .

```
LPPROPERTYPAGESITE GetPageSite();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс страницы свойств `IPropertyPageSite` .

### <a name="remarks"></a>Комментарии

Элементы управления и контейнеры взаимодействуют, чтобы пользователи могли просматривать и изменять свойства элементов управления. Элемент управления предоставляет страницы свойств, каждый из которых является объектом OLE, позволяющим пользователю изменять связанный набор свойств. Контейнер предоставляет рамку свойства, которая отображает страницы свойств. Для каждой страницы рамка свойства предоставляет сайт страницы, который поддерживает `IPropertyPageSite` интерфейс.

## <a name="colepropertypageignoreapply"></a><a name="ignoreapply"></a> COlePropertyPage:: Игнореаппли

Определяет, какие элементы управления не включают кнопку "Применить".

```cpp
void IgnoreApply(UINT nID);
```

### <a name="parameters"></a>Параметры

*nID*<br/>
Идентификатор игнорируемого элемента управления.

### <a name="remarks"></a>Комментарии

Кнопка применить страницы свойств доступна, только если значения элементов управления страницы свойств были изменены. Эта функция используется для указания элементов управления, которые не приводят к включению кнопки применить при изменении их значений.

## <a name="colepropertypageismodified"></a><a name="ismodified"></a> COlePropertyPage:: Modified

Определяет, изменил ли пользователь какие-либо значения на странице свойств.

```
BOOL IsModified();
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если страница свойств была изменена.

## <a name="colepropertypageoneditproperty"></a><a name="oneditproperty"></a> COlePropertyPage:: Онедитпроперти

Платформа вызывает эту функцию, когда нужно изменить конкретное свойство.

```
virtual BOOL OnEditProperty(DISPID dispid);
```

### <a name="parameters"></a>Параметры

*DISPID*<br/>
Идентификатор диспетчеризации изменяемого свойства.

### <a name="return-value"></a>Возвращаемое значение

Реализация по умолчанию возвращает значение FALSE. Переопределения этой функции должны возвращать значение TRUE.

### <a name="remarks"></a>Комментарии

Его можно переопределить, чтобы установить фокус на соответствующий элемент управления на странице. Реализация по умолчанию не выполняет никаких действий и возвращает значение FALSE.

## <a name="colepropertypageonhelp"></a><a name="onhelp"></a> COlePropertyPage:: OnHelp

Платформа вызывает эту функцию, когда пользователь запрашивает справку в Интернете.

```
virtual BOOL OnHelp(LPCTSTR lpszHelpDir);
```

### <a name="parameters"></a>Параметры

*лпсзелпдир*<br/>
Каталог, содержащий файл справки страницы свойств.

### <a name="return-value"></a>Возвращаемое значение

Реализация по умолчанию возвращает значение FALSE.

### <a name="remarks"></a>Комментарии

Переопределите его, если страница свойств должна выполнять какие-либо специальные действия, когда пользователь обращается к справке. Реализация по умолчанию не выполняет никаких действий и возвращает значение FALSE, что заставляет платформу вызывать WinHelp.

## <a name="colepropertypageoninitdialog"></a><a name="oninitdialog"></a> COlePropertyPage:: Онинитдиалог

Платформа вызывает эту функцию при инициализации диалогового окна страницы свойств.

```
virtual BOOL OnInitDialog();
```

### <a name="return-value"></a>Возвращаемое значение

Реализация по умолчанию возвращает значение FALSE.

### <a name="remarks"></a>Комментарии

Переопределите его, если при инициализации диалогового окна требуется какое-либо специальное действие. Реализация по умолчанию вызывает `CDialog::OnInitDialog` и возвращает значение false.

## <a name="colepropertypageonobjectschanged"></a><a name="onobjectschanged"></a> COlePropertyPage:: Онобжектсчанжед

Вызывается структурой при выборе другого элемента управления OLE с новыми свойствами.

```
virtual void OnObjectsChanged();
```

### <a name="remarks"></a>Комментарии

При просмотре свойств элемента управления OLE в среде разработки для отображения страниц свойств используется немодальное диалоговое окно. Если выбран другой элемент управления, для нового набора свойств необходимо отобразить другой набор страниц свойств. Платформа вызывает эту функцию для уведомления страницы свойств об изменении.

Переопределите эту функцию, чтобы получить уведомление об этом действии и выполнить специальные действия.

## <a name="colepropertypageonsetpagesite"></a><a name="onsetpagesite"></a> COlePropertyPage:: Онсетпажесите

Платформа вызывает эту функцию, когда рамка свойства предоставляет сайт страницы свойств.

```
virtual void OnSetPageSite();
```

### <a name="remarks"></a>Комментарии

Реализация по умолчанию загружает заголовок страницы и пытается определить размер страницы из диалогового ресурса. Переопределите эту функцию, если страница свойств требует дальнейших действий. переопределение должно вызывать реализацию базового класса.

## <a name="colepropertypagesetcontrolstatus"></a><a name="setcontrolstatus"></a> COlePropertyPage:: Сетконтролстатус

Изменяет состояние элемента управления страницы свойств.

```
BOOL SetControlStatus(
    UINT nID,
    BOOL bDirty);
```

### <a name="parameters"></a>Параметры

*nID*<br/>
Содержит идентификатор элемента управления страницы свойств.

*бдирти*<br/>
Указывает, было ли изменено поле страницы свойств. Задайте значение TRUE, если поле было изменено, и значение FALSE, если оно не было изменено.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если указанный элемент управления был задан; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Если состояние элемента управления страницы свойств — «грязный», когда страница свойств закрыта или выбрана кнопка «Применить», то свойство элемента управления будет обновлено соответствующим значением.

## <a name="colepropertypagesetdialogresource"></a><a name="setdialogresource"></a> COlePropertyPage:: Сетдиалогресаурце

Задает ресурс диалога страницы свойств.

```cpp
void SetDialogResource(HGLOBAL hDialog);
```

### <a name="parameters"></a>Параметры

*хдиалог*<br/>
Обработчик для ресурса диалога страницы свойств.

## <a name="colepropertypagesethelpinfo"></a><a name="sethelpinfo"></a> COlePropertyPage:: Сеселпинфо

Указывает сведения о подсказке, имя файла справки и контекст справки для страницы свойств.

```cpp
void SetHelpInfo(
    LPCTSTR lpszDocString,
    LPCTSTR lpszHelpFile = NULL,
    DWORD dwHelpContext = 0);
```

### <a name="parameters"></a>Параметры

*лпсздокстринг*<br/>
Строка, содержащая краткую справочную информацию для вывода в строке состояния или в другом расположении.

*лпсзелпфиле*<br/>
Имя файла справки страницы свойств.

*двхелпконтекст*<br/>
Контекст справки для страницы свойств.

## <a name="colepropertypagesetmodifiedflag"></a><a name="setmodifiedflag"></a> COlePropertyPage:: SetModifiedFlag

Указывает, изменил ли пользователь страницу свойств.

```cpp
void SetModifiedFlag(BOOL bModified = TRUE);
```

### <a name="parameters"></a>Параметры

*бмодифиед*<br/>
Задает новое значение для измененного флага страницы свойств.

## <a name="colepropertypagesetpagename"></a><a name="setpagename"></a> COlePropertyPage:: Сетпаженаме

Задает имя страницы свойств, которое обычно отображается на вкладке страницы в качестве рамки свойства.

```cpp
void SetPageName(LPCTSTR lpszPageName);
```

### <a name="parameters"></a>Параметры

*лпсзпаженаме*<br/>
Указатель на строку, содержащую имя страницы свойств.

## <a name="see-also"></a>См. также раздел

[Пример CIRC3 для MFC](../../overview/visual-cpp-samples.md)<br/>
[Пример ТЕССЕЛП для MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс CDialog](../../mfc/reference/cdialog-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CDialog](../../mfc/reference/cdialog-class.md)
