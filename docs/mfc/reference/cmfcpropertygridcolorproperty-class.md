---
description: 'Дополнительные сведения о: Кмфкпропертигридколорпроперти Class'
title: Класс Кмфкпропертигридколорпроперти
ms.date: 11/04/2016
f1_keywords:
- CMFCPropertyGridColorProperty
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::CMFCPropertyGridColorProperty
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::EnableAutomaticButton
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::EnableOtherButton
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::GetColor
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::SetColor
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::SetColumnsNumber
- AFXPROPERTYGRIDCTRL/CMFCPropertyGridColorProperty::SetOriginalValue
helpviewer_keywords:
- CMFCPropertyGridColorProperty [MFC], CMFCPropertyGridColorProperty
- CMFCPropertyGridColorProperty [MFC], EnableAutomaticButton
- CMFCPropertyGridColorProperty [MFC], EnableOtherButton
- CMFCPropertyGridColorProperty [MFC], GetColor
- CMFCPropertyGridColorProperty [MFC], SetColor
- CMFCPropertyGridColorProperty [MFC], SetColumnsNumber
- CMFCPropertyGridColorProperty [MFC], SetOriginalValue
ms.assetid: af37be93-a91e-40a2-9a65-0f3412c6f0f8
ms.openlocfilehash: 7673044a149dc1b5171167ed0854918434651dc1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334703"
---
# <a name="cmfcpropertygridcolorproperty-class"></a>Класс Кмфкпропертигридколорпроперти

Класс `CMFCPropertyGridColorProperty` поддерживает элемент управления списка свойств, открывающий диалоговое окно выбора цвета.

## <a name="syntax"></a>Синтаксис

```
class CMFCPropertyGridColorProperty : public CMFCPropertyGridProperty
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCPropertyGridColorProperty::CMFCPropertyGridColorProperty](#cmfcpropertygridcolorproperty)|Формирует объект `CMFCPropertyGridColorProperty`.|
|`CMFCPropertyGridColorProperty::~CMFCPropertyGridColorProperty`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCPropertyGridColorProperty::EnableAutomaticButton](#enableautomaticbutton)|Включает кнопку " *автоматически* " в диалоговом окне "Выбор цвета". (Стандартная автоматическая кнопка помечена как **Автоматическая**.)|
|[CMFCPropertyGridColorProperty::EnableOtherButton](#enableotherbutton)|Включает кнопку « *Дополнительно* » в диалоговом окне «Выбор цвета». (Стандартная кнопка "Дополнительно" помечена как **Дополнительные цвета**.)|
|`CMFCPropertyGridColorProperty::FormatProperty`|Форматирует текстовое представление значения свойства. (Переопределяет [кмфкпропертигридпроперти:: форматпроперти](../../mfc/reference/cmfcpropertygridproperty-class.md#formatproperty).)|
|[CMFCPropertyGridColorProperty::GetColor](#getcolor)|Возвращает текущий цвет свойства.|
|`CMFCPropertyGridColorProperty::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|
|`CMFCPropertyGridColorProperty::OnClickButton`|Вызывается платформой, когда пользователь нажимает кнопку, содержащуюся в свойстве. (Переопределяет [кмфкпропертигридпроперти:: онкликкбуттон](../../mfc/reference/cmfcpropertygridproperty-class.md#onclickbutton).)|
|`CMFCPropertyGridColorProperty::OnDrawValue`|Вызывается платформой для отображения значения свойства. (Переопределяет [кмфкпропертигридпроперти:: ондраввалуе](../../mfc/reference/cmfcpropertygridproperty-class.md#ondrawvalue).)|
|`CMFCPropertyGridColorProperty::OnEdit`|Вызывается платформой непосредственно перед изменением значения свойства пользователем. (Переопределяет [кмфкпропертигридпроперти:: onedit](../../mfc/reference/cmfcpropertygridproperty-class.md#onedit).)|
|`CMFCPropertyGridColorProperty::OnUpdateValue`|Вызывается платформой при присвоении изменяемому свойству нового значения. (Переопределяет [кмфкпропертигридпроперти:: онупдатевалуе](../../mfc/reference/cmfcpropertygridproperty-class.md#onupdatevalue).)|
|[CMFCPropertyGridColorProperty::SetColor](#setcolor)|Задает новый цвет свойства.|
|[CMFCPropertyGridColorProperty::SetColumnsNumber](#setcolumnsnumber)|Задает число столбцов в текущей таблице свойств цвета.|
|[CMFCPropertyGridColorProperty::SetOriginalValue](#setoriginalvalue)|Задает изменяемому свойству изначальное значение.|

## <a name="remarks"></a>Комментарии

Класс `CMFCPropertyGridColorProperty` поддерживает свойство цвета, которое можно добавить в элемент управления "список свойств". Дополнительные сведения см. в описании [класса кмфкпропертигридктрл](../../mfc/reference/cmfcpropertygridctrl-class.md).

## <a name="example"></a>Пример

В следующем примере демонстрируется создание объекта класса `CMFCPropertyGridColorProperty` и его настройка с помощью различных методов класса `CMFCPropertyGridColorProperty`. В коде показывается, как можно задействовать кнопки автоматического выбора и выбора другого цвета, а также выполняется назначение цвета и количества столбцов. Этот пример является частью [примера новых элементов управления](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_NewControls#13](../../mfc/reference/codesnippet/cpp/cmfcpropertygridcolorproperty-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCPropertyGridProperty](../../mfc/reference/cmfcpropertygridproperty-class.md)

[CMFCPropertyGridColorProperty](../../mfc/reference/cmfcpropertygridcolorproperty-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкспропертигридктрл. h

## <a name="cmfcpropertygridcolorpropertycmfcpropertygridcolorproperty"></a><a name="cmfcpropertygridcolorproperty"></a> Кмфкпропертигридколорпроперти:: Кмфкпропертигридколорпроперти

Формирует объект `CMFCPropertyGridColorProperty`.

```
CMFCPropertyGridColorProperty(
    const CString& strName,
    const COLORREF& color,
    CPalette* pPalette = NULL,
    LPCTSTR lpszDescr = NULL,
    DWORD_PTR dwData = 0);
```

### <a name="parameters"></a>Параметры

*strName*<br/>
[in] Имя свойства.

*color*<br/>
окне Значение цвета для свойства.

*ппалетте*<br/>
окне Указатель на палитру цветов. Значение по умолчанию — NULL.

*лпсздескр*<br/>
окне Описание свойства. Значение по умолчанию — NULL.

*двдата*<br/>
окне Данные конкретного приложения, такие как целое число или указатель на другие данные, связанные со свойством. Значение по умолчанию — 0.

## <a name="cmfcpropertygridcolorpropertyenableautomaticbutton"></a><a name="enableautomaticbutton"></a> Кмфкпропертигридколорпроперти:: Енаблеаутоматикбуттон

Включает кнопку " *автоматически* " в диалоговом окне "Выбор цвета". (Стандартная автоматическая кнопка помечена как **Автоматическая**.)

```cpp
void EnableAutomaticButton(
    LPCTSTR lpszLabel,
    COLORREF colorAutomatic,
    BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
окне Текст метки автоматической кнопки.

*колораутоматик*<br/>
окне Значение цвета RGB для цвета авто (по умолчанию).

*bEnable*<br/>
окне Значение TRUE, чтобы включить автоматическую кнопку; в противном случае — значение FALSE. Значение по умолчанию — TRUE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpropertygridcolorpropertyenableotherbutton"></a><a name="enableotherbutton"></a> Кмфкпропертигридколорпроперти:: Енаблеосербуттон

Включает кнопку « *Дополнительно* » в диалоговом окне «Выбор цвета». (Стандартная кнопка "Дополнительно" помечена как **Дополнительные цвета**.)

```cpp
void EnableOtherButton(
    LPCTSTR lpszLabel,
    BOOL bAltColorDlg = TRUE,
    BOOL bEnable = TRUE);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
окне Текст метки для другой кнопки.

*балтколордлг*<br/>
окне Значение TRUE для вывода `CMFCColorDialog` диалогового окна; Значение FALSE для вывода диалогового окна стандартный выбор цвета. Значение по умолчанию — TRUE.

*bEnable*<br/>
окне Значение TRUE, чтобы отобразить другую кнопку; в противном случае — значение FALSE.  Значение по умолчанию — TRUE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpropertygridcolorpropertygetcolor"></a><a name="getcolor"></a> Кмфкпропертигридколорпроперти:: "Color"

Возвращает текущий цвет свойства.

```
COLORREF GetColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение цвета RGB.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpropertygridcolorpropertysetcolor"></a><a name="setcolor"></a> Кмфкпропертигридколорпроперти:: Сетколор

Задает новый цвет свойства.

```cpp
void SetColor(COLORREF color);
```

### <a name="parameters"></a>Параметры

*color*<br/>
окне Значение цвета RGB.

### <a name="remarks"></a>Комментарии

## <a name="cmfcpropertygridcolorpropertysetcolumnsnumber"></a><a name="setcolumnsnumber"></a> Кмфкпропертигридколорпроперти:: Сетколумнснумбер

Задает число столбцов в текущей таблице свойств цвета.

```cpp
void SetColumnsNumber(int nColumnsNumber);
```

### <a name="parameters"></a>Параметры

*нколумнснумбер*<br/>
окне Предпочтительное число столбцов в сетке свойств цвета.

### <a name="remarks"></a>Комментарии

Этот метод задает значение `m_nColumnsNumber` защищенного элемента данных.

## <a name="cmfcpropertygridcolorpropertysetoriginalvalue"></a><a name="setoriginalvalue"></a> Кмфкпропертигридколорпроперти:: Сеторигиналвалуе

Задает изменяемому свойству изначальное значение.

```
virtual void SetOriginalValue(const COleVariant& varValue);
```

### <a name="parameters"></a>Параметры

*varValue*<br/>
окне Значение.

### <a name="remarks"></a>Комментарии

Используйте метод [кмфкпропертигридпроперти:: ресеторигиналвалуе](../../mfc/reference/cmfcpropertygridproperty-class.md#resetoriginalvalue) , чтобы сбросить исходное значение редактируемого свойства.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкпропертигридктрл](../../mfc/reference/cmfcpropertygridctrl-class.md)<br/>
[Класс Кмфкпропертигридпроперти](../../mfc/reference/cmfcpropertygridproperty-class.md)
