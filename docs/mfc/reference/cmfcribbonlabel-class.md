---
description: 'Дополнительные сведения о: Кмфкриббонлабел Class'
title: Класс Кмфкриббонлабел
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonLabel
- AFXRIBBONLABEL/CMFCRibbonLabel
- AFXRIBBONLABEL/CMFCRibbonLabel::CMFCRibbonLabel
- AFXRIBBONLABEL/CMFCRibbonLabel::SetACCData
helpviewer_keywords:
- CMFCRibbonLabel [MFC], CMFCRibbonLabel
- CMFCRibbonLabel [MFC], SetACCData
ms.assetid: 0346c891-83bf-4f20-b8a1-c84cf2aadced
ms.openlocfilehash: 0699e76dfe90b87cd813d18d076adf23f8512bee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321830"
---
# <a name="cmfcribbonlabel-class"></a>Класс Кмфкриббонлабел

Реализует недоступную для щелчка текстовую метку для ленты.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonLabel : public CMFCRibbonButton
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонлабел:: Кмфкриббонлабел](#cmfcribbonlabel)|Создает и инициализирует `CMFCRibbonLabel` объект с указанной текстовой строкой.|
|`CMFCRibbonLabel::~CMFCRibbonLabel`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|`CMFCRibbonLabel::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|`CMFCRibbonLabel::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|
|[Кмфкриббонлабел:: Сетаккдата](#setaccdata)|Определяет данные о специальных возможностях для текущего элемента метки ленты. (Переопределяет [CMFCRibbonButton:: сетаккдата](../../mfc/reference/cmfcribbonbutton-class.md#setaccdata).)|

### <a name="remarks"></a>Комментарии

После создания метки ленты добавьте ее на панель, вызвав [CMFCRibbonPanel:: Add](../../mfc/reference/cmfcribbonpanel-class.md#add).

На панель быстрого доступа нельзя добавить метку ленты.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)

[CMFCRibbonLabel](../../mfc/reference/cmfcribbonlabel-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонлабел. h

## <a name="cmfcribbonlabelcmfcribbonlabel"></a><a name="cmfcribbonlabel"></a> Кмфкриббонлабел:: Кмфкриббонлабел

Создает и инициализирует объект [кмфкриббонлабел](../../mfc/reference/cmfcribbonlabel-class.md) , отображающий указанную текстовую строку.

```
CMFCRibbonLabel(
    LPCTSTR lpszText,
    BOOL bIsMultiLine = FALSE);
```

### <a name="parameters"></a>Параметры

*lpszText*<br/>
окне Текст, отображаемый в метке.

*бисмултилине*<br/>
окне Значение TRUE, чтобы указать, что метка является многострочной меткой; в противном случае — значение FALSE.

## <a name="cmfcribbonlabelsetaccdata"></a><a name="setaccdata"></a> Кмфкриббонлабел:: Сетаккдата

Определяет данные о специальных возможностях для текущего элемента метки ленты.

```
virtual BOOL SetACCData(
    CWnd* pParent,
    CAccessibilityData& data);
```

### <a name="parameters"></a>Параметры

*ппарент*<br/>
окне Представляет родительское окно Метки текущей ленты.

*data*<br/>
заполняет Объект типа `CAccessibilityData` , заполненный данными о специальных возможностях текущей метки ленты.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если параметр *данных* успешно заполнен данными о специальных возможностях текущей метки ленты. в противном случае — значение FALSE.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)
