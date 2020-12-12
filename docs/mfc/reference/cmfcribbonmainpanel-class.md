---
description: 'Дополнительные сведения о: CMFCRibbonMainPanel Class'
title: Класс CMFCRibbonMainPanel
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonMainPanel
- AFXRIBBONMAINPANEL/CMFCRibbonMainPanel
- AFXRIBBONMAINPANEL/CMFCRibbonMainPanel::Add
- AFXRIBBONMAINPANEL/CMFCRibbonMainPanel::AddRecentFilesList
- AFXRIBBONMAINPANEL/CMFCRibbonMainPanel::AddToBottom
- AFXRIBBONMAINPANEL/CMFCRibbonMainPanel::AddToRight
- AFXRIBBONMAINPANEL/CMFCRibbonMainPanel::GetCommandsFrame
helpviewer_keywords:
- CMFCRibbonMainPanel [MFC], Add
- CMFCRibbonMainPanel [MFC], AddRecentFilesList
- CMFCRibbonMainPanel [MFC], AddToBottom
- CMFCRibbonMainPanel [MFC], AddToRight
- CMFCRibbonMainPanel [MFC], GetCommandsFrame
ms.assetid: 1af78798-5e75-4365-9c81-a54aa5679602
ms.openlocfilehash: 823a1ce8a8684ca791f838346a1fb50727096a62
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321816"
---
# <a name="cmfcribbonmainpanel-class"></a>Класс CMFCRibbonMainPanel

Реализует панель ленты, которая отображается при нажатии кнопки [кмфкриббонаппликатионбуттон](../../mfc/reference/cmfcribbonapplicationbutton-class.md).

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonMainPanel : public CMFCRibbonPanel
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCRibbonMainPanel::CMFCRibbonMainPanel`|Конструктор по умолчанию.|
|`CMFCRibbonMainPanel::~CMFCRibbonMainPanel`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonMainPanel:: Add](#add)|Добавляет элемент ленты в левую область панели кнопки приложения. (Переопределяет [CMFCRibbonPanel:: Add](../../mfc/reference/cmfcribbonpanel-class.md#add).)|
|[CMFCRibbonMainPanel:: Аддрецентфилеслист](#addrecentfileslist)|Добавляет текстовую строку в меню списка последних файлов.|
|[CMFCRibbonMainPanel:: Аддтоботтом](#addtobottom)|Добавляет элемент лента в нижнюю область панели приложения ленты.|
|[CMFCRibbonMainPanel:: Аддторигхт](#addtoright)|Добавляет элемент ленты в правую панель панели кнопки приложения.|
|`CMFCRibbonMainPanel::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|[CMFCRibbonMainPanel:: Жеткоммандсфраме](#getcommandsframe)|Возвращает прямоугольник, представляющий область главной панели ленты.|
|`CMFCRibbonMainPanel::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|

## <a name="remarks"></a>Комментарии

Платформа отображает `CMFCRibbonMainPanel` при открытии панели приложения. Он содержит три панели:

- В левой области содержатся команды, связанные с файлами, такие как **Открытие**, **Сохранение**, **Печать** и **закрытие**. Чтобы добавить команду в эту область, вызовите метод [CMFCRibbonMainPanel:: Add](#add).

- Правая панель содержит параметры, которые изменяют команду, которую вы щелкнули в левой области. Например, если нажать кнопку **Сохранить как** в левой области, на правой панели могут отображаться доступные типы файлов. Чтобы добавить элемент в эту панель, вызовите метод [CMFCRibbonMainPanel:: аддторигхт](#addtoright).

- Нижняя панель содержит кнопки, позволяющие изменить параметры приложения и выйти из программы. Чтобы добавить элемент в эту панель, вызовите метод [CMFCRibbonMainPanel:: аддтоботтом](#addtobottom).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonPanel](../../mfc/reference/cmfcribbonpanel-class.md)

[CMFCRibbonMainPanel](../../mfc/reference/cmfcribbonmainpanel-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонмаинпанел. h

## <a name="cmfcribbonmainpaneladd"></a><a name="add"></a> CMFCRibbonMainPanel:: Add

Добавляет элемент ленты в левую область панели кнопки приложения.

```
virtual void Add(CMFCRibbonBaseElement* pElem);
```

### <a name="parameters"></a>Параметры

*пелем*<br/>
[вход, выход] Указатель на элемент ленты, добавляемый на главную панель.

### <a name="remarks"></a>Комментарии

Добавляет элемент ленты на панель. Элементы, добавленные с помощью этого метода, будут расположены в левом столбце главной панели.

## <a name="cmfcribbonmainpaneladdrecentfileslist"></a><a name="addrecentfileslist"></a> CMFCRibbonMainPanel:: Аддрецентфилеслист

Добавляет текстовую строку в меню списка последних файлов.

```cpp
void AddRecentFilesList(
    LPCTSTR lpszLabel,
    int nWidth = 300);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
Указывает строку, добавляемую в список последних файлов.

*нвидс*<br/>
Задает ширину (в пикселях) панели списка последних файлов.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonmainpaneladdtobottom"></a><a name="addtobottom"></a> CMFCRibbonMainPanel:: Аддтоботтом

Добавляет элемент лента в нижнюю область панели приложения ленты.

```cpp
void AddToBottom(CMFCRibbonMainPanelButton* pElem);
```

### <a name="parameters"></a>Параметры

*пелем*<br/>
[вход, выход] Указатель на элемент ленты, добавляемый в нижнюю часть главной панели.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonmainpaneladdtoright"></a><a name="addtoright"></a> CMFCRibbonMainPanel:: Аддторигхт

Добавляет элемент ленты в правую панель панели кнопки приложения.

```cpp
void AddToRight(
    CMFCRibbonBaseElement* pElem,
    int nWidth = 300);
```

### <a name="parameters"></a>Параметры

*пелем*<br/>
Указатель на элемент ленты, добавляемый в правую часть главной панели.

*нвидс*<br/>
Задает ширину (в пикселях) правой панели.

### <a name="remarks"></a>Комментарии

Эта функция используется для добавления элемента ленты на правую панель. На правой панели обычно отображается список последние файлы, но можно добавить любой другой элемент ленты.

## <a name="cmfcribbonmainpanelgetcommandsframe"></a><a name="getcommandsframe"></a> CMFCRibbonMainPanel:: Жеткоммандсфраме

Возвращает прямоугольник, представляющий область главной панели ленты.

```
CRect GetCommandsFrame() const;
```

### <a name="return-value"></a>Возвращаемое значение

Прямоугольник, представляющий область главной панели ленты.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCRibbonPanel](../../mfc/reference/cmfcribbonpanel-class.md)
