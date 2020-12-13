---
description: 'Дополнительные сведения о: Кмфктулбарфонтсизекомбобокс Class'
title: Класс Кмфктулбарфонтсизекомбобокс
ms.date: 11/04/2016
f1_keywords:
- CMFCToolBarFontSizeComboBox
- AFXTOOLBARFONTCOMBOBOX/CMFCToolBarFontSizeComboBox
- AFXTOOLBARFONTCOMBOBOX/CMFCToolBarFontSizeComboBox::CMFCToolBarFontSizeComboBox
- AFXTOOLBARFONTCOMBOBOX/CMFCToolBarFontSizeComboBox::GetTwipSize
- AFXTOOLBARFONTCOMBOBOX/CMFCToolBarFontSizeComboBox::RebuildFontSizes
- AFXTOOLBARFONTCOMBOBOX/CMFCToolBarFontSizeComboBox::SetTwipSize
helpviewer_keywords:
- CMFCToolBarFontSizeComboBox [MFC], CMFCToolBarFontSizeComboBox
- CMFCToolBarFontSizeComboBox [MFC], GetTwipSize
- CMFCToolBarFontSizeComboBox [MFC], RebuildFontSizes
- CMFCToolBarFontSizeComboBox [MFC], SetTwipSize
ms.assetid: 72e0c44c-6a0e-4194-a71f-ab64e3afb9b5
ms.openlocfilehash: a355e62f2ef538372d70b9b2b393bc16bff2ef4b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331742"
---
# <a name="cmfctoolbarfontsizecombobox-class"></a>Класс Кмфктулбарфонтсизекомбобокс

Кнопка на панели инструментов, содержащая элемент управления "поле со списком", позволяющий пользователю выбрать размер шрифта.

## <a name="syntax"></a>Синтаксис

```
class CMFCToolBarFontSizeComboBox : public CMFCToolBarComboBoxButton
```

## <a name="members"></a>Члены

### <a name="protected-constructors"></a>Защищенные конструкторы

|Имя|Описание|
|----------|-----------------|
|[Кмфктулбарфонтсизекомбобокс:: Кмфктулбарфонтсизекомбобокс](#cmfctoolbarfontsizecombobox)|Формирует объект `CMFCToolBarFontSizeComboBox`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфктулбарфонтсизекомбобокс:: Жеттвипсизе](#gettwipsize)|Возвращает выбранный размер шрифта в твипах.|
|[Кмфктулбарфонтсизекомбобокс:: Ребуилдфонтсизес](#rebuildfontsizes)|Заполняет список полей со списком всеми поддерживаемыми размерами шрифтов для указанного шрифта.|
|[Кмфктулбарфонтсизекомбобокс:: Сеттвипсизе](#settwipsize)|Задает размер шрифта в твипах.|

## <a name="remarks"></a>Комментарии

Объект можно использовать `CMFCToolBarFontSizeComboBox` вместе с объектом [класса кмфктулбарфонткомбобокс](../../mfc/reference/cmfctoolbarfontcombobox-class.md) , чтобы позволить пользователю выбрать шрифт и размер шрифта.

Можно добавить кнопку поля со списком размер шрифта на панель инструментов при добавлении кнопки поля со списком шрифтов. Дополнительные сведения см. в разделе [класс кмфктулбарфонткомбобокс](../../mfc/reference/cmfctoolbarfontcombobox-class.md).

Когда пользователь выбирает новый шрифт в `CMFCToolBarFontComboBox` объекте, можно заполнить поле со списком размер шрифта поддерживаемыми размерами для этого шрифта с помощью метода [кмфктулбарфонтсизекомбобокс:: ребуилдфонтсизес](#rebuildfontsizes) .

## <a name="example"></a>Пример

В следующем примере показано, как использовать различные методы в `CMFCToolBarFontSizeComboBox` классе для настройки `CMFCToolBarFontSizeComboBox` объекта. В примере показано, как извлечь размер шрифта в твипах из текстового поля, заполнить поле со списком размер шрифта всеми допустимыми размерами данного шрифта и указать размер шрифта в твипах. Этот фрагмент кода входит в состав [примера Word Pad](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_WordPad#8](../../mfc/reference/codesnippet/cpp/cmfctoolbarfontsizecombobox-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCToolBarButton](../../mfc/reference/cmfctoolbarbutton-class.md)

[кмфктулбаркомбобоксбуттон](../../mfc/reference/cmfctoolbarcomboboxbutton-class.md)

[кмфктулбарфонтсизекомбобокс](../../mfc/reference/cmfctoolbarfontsizecombobox-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкстулбарфонткомбобокс. h

## <a name="cmfctoolbarfontsizecomboboxcmfctoolbarfontsizecombobox"></a><a name="cmfctoolbarfontsizecombobox"></a> Кмфктулбарфонтсизекомбобокс:: Кмфктулбарфонтсизекомбобокс

Формирует объект `CMFCToolBarFontSizeComboBox`.

```
CMFCToolBarFontSizeComboBox();
```

## <a name="cmfctoolbarfontsizecomboboxgettwipsize"></a><a name="gettwipsize"></a> Кмфктулбарфонтсизекомбобокс:: Жеттвипсизе

Получает размер шрифта в твипах из текстового поля поля со списком размер шрифта.

```
int GetTwipSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Если возвращаемое значение положительное, то это размер шрифта в твипах. Значение-1, если текстовое поле со списком пустое. При возникновении ошибки — 2.

## <a name="cmfctoolbarfontsizecomboboxrebuildfontsizes"></a><a name="rebuildfontsizes"></a> Кмфктулбарфонтсизекомбобокс:: Ребуилдфонтсизес

Заполняет поле со списком размера шрифта всеми допустимыми размерами данного шрифта.

```cpp
void RebuildFontSizes(const CString& strFontName);
```

### <a name="parameters"></a>Параметры

*стрфонтнаме*<br/>
окне Задает имя шрифта.

### <a name="remarks"></a>Комментарии

Вызывайте эту функцию, если нужно синхронизировать выборку в поле со списком шрифтов и поле со списком размер шрифта, например [класс кмфктулбарфонткомбобокс](../../mfc/reference/cmfctoolbarfontcombobox-class.md).

## <a name="cmfctoolbarfontsizecomboboxsettwipsize"></a><a name="settwipsize"></a> Кмфктулбарфонтсизекомбобокс:: Сеттвипсизе

Округляет указанный размер (в твипах) до ближайшего размера в точках, а затем задает для выбранного размера в поле со списком указанное значение.

```cpp
void SetTwipSize(int nSize);
```

### <a name="parameters"></a>Параметры

*нсизе*<br/>
окне Задает размер шрифта (в твипах) для задания.

### <a name="remarks"></a>Комментарии

Предыдущий допустимый размер шрифта можно получить позже, вызвав метод [кмфктулбарфонтсизекомбобокс:: жеттвипсизе](#gettwipsize) .

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)<br/>
[Класс CMFCToolBarButton](../../mfc/reference/cmfctoolbarbutton-class.md)<br/>
[Класс Кмфктулбаркомбобоксбуттон](../../mfc/reference/cmfctoolbarcomboboxbutton-class.md)<br/>
[Класс Кмфкфонтинфо](../../mfc/reference/cmfcfontinfo-class.md)<br/>
[CMFCToolBar:: Реплацебуттон](../../mfc/reference/cmfctoolbar-class.md#replacebutton)<br/>
[Пошаговое руководство. размещение элементов управления на панелях инструментов](../../mfc/walkthrough-putting-controls-on-toolbars.md)
