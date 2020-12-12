---
description: 'Дополнительные сведения о: Кмфкриббонконтексткаптион Class'
title: Класс Кмфкриббонконтексткаптион
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonContextCaption
- AFXRIBBONBAR/CMFCRibbonContextCaption
- AFXRIBBONBAR/CMFCRibbonContextCaption::GetColor
- AFXRIBBONBAR/CMFCRibbonContextCaption::GetRightTabX
helpviewer_keywords:
- CMFCRibbonContextCaption [MFC], GetColor
- CMFCRibbonContextCaption [MFC], GetRightTabX
ms.assetid: cce2c0a2-8370-4266-997e-f8d0eeb3d616
ms.openlocfilehash: fa4134b89055274e4f44bef1150518207e06143e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97293629"
---
# <a name="cmfcribboncontextcaption-class"></a>Класс Кмфкриббонконтексткаптион

Реализует цветной заголовок, который отображается в верхней части категории "лента" или категории "контекст".

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonContextCaption : public CMFCRibbonButton
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|`CMFCRibbonContextCaption::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|[CMFCRibbonContextCaption::GetColor](#getcolor)|Возвращает цвет заголовка.|
|[CMFCRibbonContextCaption::GetRightTabX](#getrighttabx)||
|`CMFCRibbonContextCaption::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|

## <a name="remarks"></a>Комментарии

Создать экземпляр этого класса напрямую невозможно. Класс [класса CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md) использует этот класс для внутренних целей для добавления цвета к категориям ленты.

Чтобы задать цвет для категорий ленты, вызовите метод [кмфкриббонкатегори:: сеттабколор](../../mfc/reference/cmfcribboncategory-class.md#settabcolor). Чтобы задать цвет для контекстных категорий, вызовите [CMFCRibbonBar:: аддконтексткатегори](../../mfc/reference/cmfcribbonbar-class.md#addcontextcategory).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)

[CMFCRibbonContextCaption](../../mfc/reference/cmfcribboncontextcaption-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонбар. h

## <a name="cmfcribboncontextcaptiongetcolor"></a><a name="getcolor"></a> Кмфкриббонконтексткаптион:: "Color"

Возвращает цвет фона заголовка.

```
AFX_RibbonCategoryColor GetColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение может быть одним из следующих перечисляемых значений:

- `AFX_CategoryColor_None`

- `AFX_CategoryColor_Red`

- `AFX_CategoryColor_Orange`

- `AFX_CategoryColor_Yellow`

- `AFX_CategoryColor_Green`

- `AFX_CategoryColor_Blue`

- `AFX_CategoryColor_Indigo`

- `AFX_CategoryColor_Violet`

### <a name="remarks"></a>Комментарии

Цвет заголовка можно задать, вызвав [кмфкриббонкатегори:: сеттабколор](../../mfc/reference/cmfcribboncategory-class.md#settabcolor) или [CMFCRibbonBar:: аддконтексткатегори](../../mfc/reference/cmfcribbonbar-class.md#addcontextcategory).

## <a name="cmfcribboncontextcaptiongetrighttabx"></a><a name="getrighttabx"></a> Кмфкриббонконтексткаптион:: Жетригхттабкс

Извлекает позицию правого края вкладки на ленте категории.

```
int GetRightTabX() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает правое значение X охватывающего прямоугольника `CMFCRibbonCategory` вкладки ленты объекта или значение-1, если вкладка обрезана.

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)<br/>
[Класс Кмфкриббонкатегори](../../mfc/reference/cmfcribboncategory-class.md)<br/>
[Класс CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md)
