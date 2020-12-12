---
description: 'Дополнительные сведения о: Кмфкриббонундобуттон Class'
title: Класс Кмфкриббонундобуттон
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonUndoButton
- AFXRIBBONUNDOBUTTON/CMFCRibbonUndoButton
- AFXRIBBONUNDOBUTTON/CMFCRibbonUndoButton::CMFCRibbonUndoButton
- AFXRIBBONUNDOBUTTON/CMFCRibbonUndoButton::AddUndoAction
- AFXRIBBONUNDOBUTTON/CMFCRibbonUndoButton::CleanUpUndoList
- AFXRIBBONUNDOBUTTON/CMFCRibbonUndoButton::GetActionNumber
- AFXRIBBONUNDOBUTTON/CMFCRibbonUndoButton::HasMenu
helpviewer_keywords:
- CMFCRibbonUndoButton [MFC], CMFCRibbonUndoButton
- CMFCRibbonUndoButton [MFC], AddUndoAction
- CMFCRibbonUndoButton [MFC], CleanUpUndoList
- CMFCRibbonUndoButton [MFC], GetActionNumber
- CMFCRibbonUndoButton [MFC], HasMenu
ms.assetid: 5c42adf7-871d-4239-901e-47ae7fb816fc
ms.openlocfilehash: 8bfc02b61160a5f11a6913736c5dc784c4d00ce4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264938"
---
# <a name="cmfcribbonundobutton-class"></a>Класс Кмфкриббонундобуттон

`CMFCRibbonUndoButton`Класс реализует кнопку раскрывающегося списка, содержащую последние команды пользователя. Пользователи могут выбрать одну или несколько последних команд из раскрывающегося списка, чтобы либо повторить, либо отменить их.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonUndoButton : public CMFCRibbonGallery
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонундобуттон:: Кмфкриббонундобуттон](#cmfcribbonundobutton)|Конструирует новый объект, `CMFCRibbonUndoButton` используя указанный идентификатор команды, текстовую метку и изображения из списка изображений родительского объекта.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонундобуттон:: Аддундоактион](#addundoaction)|Добавляет новое действие в список действий.|
|[Кмфкриббонундобуттон:: Клеанупундолист](#cleanupundolist)|Очищает список действий, который является раскрывающимся списком.|
|[Кмфкриббонундобуттон:: Жетактионнумбер](#getactionnumber)|Определяет число элементов, выбранных пользователем в раскрывающемся списке.|
|[Кмфкриббонундобуттон:: Хасмену](#hasmenu)|Указывает, содержит ли объект меню.|

## <a name="remarks"></a>Комментарии

`CMFCRibbonUndoButton`Класс использует стек для представления раскрывающегося списка.

## <a name="example"></a>Пример

В следующем примере показано, как создать объект `CMFCRibbonUndoButton` класса и добавить новое действие в список действий. Этот фрагмент кода является частью [примера мини-приложений ленты](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_RibbonGadgets#2](../../mfc/reference/codesnippet/cpp/cmfcribbonundobutton-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)

[CMFCRibbonGallery](../../mfc/reference/cmfcribbongallery-class.md)

[CMFCRibbonUndoButton](../../mfc/reference/cmfcribbonundobutton-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонундобуттон. h

## <a name="cmfcribbonundobuttonaddundoaction"></a><a name="addundoaction"></a> Кмфкриббонундобуттон:: Аддундоактион

Добавляет новое действие в список действий.

```cpp
void AddUndoAction(LPCTSTR lpszLabel);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
окне Метка действия, которая будет отображаться в раскрывающемся списке.

## <a name="cmfcribbonundobuttoncleanupundolist"></a><a name="cleanupundolist"></a> Кмфкриббонундобуттон:: Клеанупундолист

Очищает список действий, который является раскрывающимся списком.

```cpp
void CleanUpUndoList();
```

## <a name="cmfcribbonundobuttoncmfcribbonundobutton"></a><a name="cmfcribbonundobutton"></a> Кмфкриббонундобуттон:: Кмфкриббонундобуттон

Конструирует новый объект, `CMFCRibbonUndoButton` используя указанный идентификатор команды, текстовую метку и изображения из списка изображений родительского объекта.

```
CMFCRibbonUndoButton(
    UINT nID,
    LPCTSTR lpszText,
    int nSmallImageIndex=-1,
    int nLargeImageIndex=-1);

CMFCRibbonUndoButton(
    UINT nID,
    LPCTSTR lpszText,
    HICON hIcon);
```

### <a name="parameters"></a>Параметры

*nID*<br/>
окне Указывает идентификатор команды.

*lpszText*<br/>
окне Задает текстовую метку кнопки.

*нсмаллимажеиндекс*<br/>
окне Отсчитываемый от нуля индекс в списке изображений родительского объекта для мелкого изображения кнопки.

*нларжеимажеиндекс*<br/>
окне Отсчитываемый от нуля индекс в списке изображений родительского объекта для большого изображения кнопки.

*hIcon*<br/>
окне Маркер значка, который можно использовать в качестве изображения кнопки.

## <a name="cmfcribbonundobuttongetactionnumber"></a><a name="getactionnumber"></a> Кмфкриббонундобуттон:: Жетактионнумбер

Определяет число элементов, выбранных пользователем в раскрывающемся списке.

```
int GetActionNumber() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число элементов, выбранных пользователем.

## <a name="cmfcribbonundobuttonhasmenu"></a><a name="hasmenu"></a> Кмфкриббонундобуттон:: Хасмену

Указывает, содержит ли объект меню.

```
virtual BOOL HasMenu() const;
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение TRUE.

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкриббонгаллери](../../mfc/reference/cmfcribbongallery-class.md)<br/>
[Класс CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)
