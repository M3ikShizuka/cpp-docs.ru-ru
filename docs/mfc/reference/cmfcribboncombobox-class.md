---
description: 'Дополнительные сведения о: Кмфкриббонкомбобокс Class'
title: Класс Кмфкриббонкомбобокс
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonComboBox
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::CMFCRibbonComboBox
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::AddItem
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::DeleteItem
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::EnableDropDownListResize
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::FindItem
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::GetCount
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::GetCurSel
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::GetDropDownHeight
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::GetIntermediateSize
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::GetItem
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::GetItemData
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::HasEditBox
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::IsResizeDropDownList
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::OnSelectItem
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::RemoveAllItems
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::SelectItem
- AFXRIBBONCOMBOBOX/CMFCRibbonComboBox::SetDropDownHeight
helpviewer_keywords:
- CMFCRibbonComboBox [MFC], CMFCRibbonComboBox
- CMFCRibbonComboBox [MFC], AddItem
- CMFCRibbonComboBox [MFC], DeleteItem
- CMFCRibbonComboBox [MFC], EnableDropDownListResize
- CMFCRibbonComboBox [MFC], FindItem
- CMFCRibbonComboBox [MFC], GetCount
- CMFCRibbonComboBox [MFC], GetCurSel
- CMFCRibbonComboBox [MFC], GetDropDownHeight
- CMFCRibbonComboBox [MFC], GetIntermediateSize
- CMFCRibbonComboBox [MFC], GetItem
- CMFCRibbonComboBox [MFC], GetItemData
- CMFCRibbonComboBox [MFC], HasEditBox
- CMFCRibbonComboBox [MFC], IsResizeDropDownList
- CMFCRibbonComboBox [MFC], OnSelectItem
- CMFCRibbonComboBox [MFC], RemoveAllItems
- CMFCRibbonComboBox [MFC], SelectItem
- CMFCRibbonComboBox [MFC], SetDropDownHeight
ms.assetid: 9b29a6a4-cf17-4152-9b13-0bf90784b30d
ms.openlocfilehash: be4078145817d06fafddb76f2cefbd0df0083503
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97293670"
---
# <a name="cmfcribboncombobox-class"></a>Класс Кмфкриббонкомбобокс

`CMFCRibbonComboBox`Класс реализует элемент управления "поле со списком", который можно добавить на панель ленты, на панель ленты или в всплывающее меню ленты.

## <a name="syntax"></a>Синтаксис

```cpp
class CMFCRibbonComboBox : public CMFCRibbonEdit
```

## <a name="members"></a>Члены

### <a name="constructors"></a>Конструкторы

|Имя|Описание|
|----------|-----------------|
|[Кмфкриббонкомбобокс:: Кмфкриббонкомбобокс](#cmfcribboncombobox)|Конструирует объект Кмфкриббонкомбобокс.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонкомбобокс:: AddItem](#additem)|Добавляет уникальный элемент в список.|
|[Кмфкриббонкомбобокс::D Елетеитем](#deleteitem)|Удаляет указанный элемент из списка.|
|[Кмфкриббонкомбобокс:: Енабледропдовнлистресизе](#enabledropdownlistresize)|Указывает, может ли список изменять размер при падении.|
|[Кмфкриббонкомбобокс:: FindItem](#finditem)|Возвращает индекс первого элемента в списке, соответствующего указанной строке.|
|[Кмфкриббонкомбобокс:: NOCOUNT](#getcount)|Возвращает количество элементов в списке.|
|[Кмфкриббонкомбобокс:: рекурсивно](#getcursel)|Возвращает индекс выбранного в данный момент элемента в списке.|
|[Кмфкриббонкомбобокс:: Жетдропдовнхеигхт](#getdropdownheight)|Возвращает высоту поля со списком при перетаскивании списка.|
|[Кмфкриббонкомбобокс:: GetIntermediateSize](#getintermediatesize)|Возвращает размер поля со списком, отображаемого в промежуточном режиме.|
|[Кмфкриббонкомбобокс:: DataItem](#getitem)|Возвращает строку, связанную с элементом по указанному индексу в поле со списком.|
|[Кмфкриббонкомбобокс:: Жетитемдата](#getitemdata)|Возвращает данные, связанные с элементом по указанному индексу в списке.|
|[Кмфкриббонкомбобокс:: Хаседитбокс](#haseditbox)|Указывает, содержит ли элемент управления поле ввода.|
|[Кмфкриббонкомбобокс:: Исресизедропдовнлист](#isresizedropdownlist)|Указывает, можно ли изменить размер окна списка.|
|[Кмфкриббонкомбобокс:: Онселектитем](#onselectitem)|Вызывается платформой, когда пользователь выбирает элемент в списке.|
|[Кмфкриббонкомбобокс:: Ремовеаллитемс](#removeallitems)|Удаляет все элементы из списка и очищает поле ввода.|
|[Кмфкриббонкомбобокс:: Селектитем](#selectitem)|Выбирает элемент в списке.|
|[Кмфкриббонкомбобокс:: Сетдропдовнхеигхт](#setdropdownheight)|Задает высоту поля со списком при его перетаскивании.|

## <a name="remarks"></a>Комментарии

Поле со списком ленты состоит из списка, объединенного с статической меткой или меткой, которую пользователь может изменять. При создании поля со списком ленты необходимо указать нужный тип.

## <a name="example"></a>Пример

В следующем примере показано, как создать объект `CMFCRibbonComboBox` класса, добавить элемент в поле со списком, выбрать элемент в поле со списком и добавить поле со списком на панель.

[!code-cpp[NVC_MFC_RibbonApp#11](../../mfc/reference/codesnippet/cpp/cmfcribboncombobox-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)

[CMFCRibbonEdit](../../mfc/reference/cmfcribbonedit-class.md)

[CMFCRibbonComboBox](../../mfc/reference/cmfcribboncombobox-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонкомбобокс. h

## <a name="cmfcribboncomboboxadditem"></a><a name="additem"></a> Кмфкриббонкомбобокс:: AddItem

Добавляет уникальный элемент в список.

```cpp
virtual INT_PTR AddItem(
    LPCTSTR lpszItem,
    DWORD_PTR dwData=0);
```

### <a name="parameters"></a>Параметры

*лпсзитем*<br/>
окне Строка добавляемого элемента.

*двдата*<br/>
окне Данные, связанные с добавляемым элементом.

### <a name="return-value"></a>Возвращаемое значение

Отсчитываемый от нуля индекс добавляемого элемента.

## <a name="cmfcribboncomboboxcmfcribboncombobox"></a><a name="cmfcribboncombobox"></a> Кмфкриббонкомбобокс:: Кмфкриббонкомбобокс

Формирует объект `CMFCRibbonComboBox`.

```cpp
public:
CMFCRibbonComboBox(
    UINT nID,
    BOOL bHasEditBox=TRUE,
    Int nWidth=-1,
    LPCTSTR lpszLabel=NULL,
    Int nImage=-1);

protected:
CMFCRibbonComboBox();
```

### <a name="parameters"></a>Параметры

*nID*<br/>
окне Идентификатор поля со списком.

*бхаседитбокс*<br/>
окне Значение TRUE, если требуется поле ввода в элементе управления; В противном случае — значение FALSE.

*нвидс*<br/>
окне Ширина поля со списком в пикселях; или-1 для ширины по умолчанию.

*лпсзлабел*<br/>
окне Отображаемая метка поля со списком.

*нимаже*<br/>
окне Маленький индекс изображения в поле со списком.

### <a name="remarks"></a>Комментарии

Ширина по умолчанию — 108 пикселей.

## <a name="cmfcribboncomboboxdeleteitem"></a><a name="deleteitem"></a> Кмфкриббонкомбобокс::D Елетеитем

Удаляет указанный элемент из списка.

```cpp
BOOL DeleteItem(int iIndex);
BOOL DeleteItem(DWORD_PTR dwData);

BOOL DeleteItem(LPCTSTR lpszText);
```

### <a name="parameters"></a>Параметры

*ииндекс*<br/>
окне Отсчитываемый от нуля индекс удаляемого элемента.

*двдата*<br/>
окне Данные, связанные с удаляемым элементом.

*lpszText*<br/>
окне Строка удаляемого элемента. Если имеется несколько элементов с одной и той же строкой, первый элемент удаляется.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если указанный элемент был удален; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncomboboxenabledropdownlistresize"></a><a name="enabledropdownlistresize"></a> Кмфкриббонкомбобокс:: Енабледропдовнлистресизе

Указывает, может ли список изменять размер при падении.

```cpp
void EnableDropDownListResize(BOOL bEnable=FALSE);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
окне Значение TRUE, чтобы включить изменение размера; Значение FALSE, чтобы отключить изменение размера.

### <a name="remarks"></a>Комментарии

Если изменение размера включено, размер списка изменится в соответствии с отображаемыми элементами.

## <a name="cmfcribboncomboboxfinditem"></a><a name="finditem"></a> Кмфкриббонкомбобокс:: FindItem

Возвращает индекс первого элемента в списке, соответствующего указанной строке.

```cpp
int FindItem(LPCTSTR lpszText) const;
```

### <a name="parameters"></a>Параметры

*lpszText*<br/>
окне Строка элемента в списке.

### <a name="return-value"></a>Возвращаемое значение

Отсчитываемый от нуля индекс элемента; значение-1, если элемент не найден.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncomboboxgetcount"></a><a name="getcount"></a> Кмфкриббонкомбобокс:: NOCOUNT

Возвращает количество элементов в списке.

```cpp
INT_PTR GetCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число элементов в списке или значение 0, если список не содержит элементов.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncomboboxgetcursel"></a><a name="getcursel"></a> Кмфкриббонкомбобокс:: рекурсивно

Возвращает индекс выбранного в данный момент элемента в списке.

```cpp
int GetCurSel() const;
```

### <a name="return-value"></a>Возвращаемое значение

Отсчитываемый от нуля индекс текущего выбранного элемента в списке; или-1, если элемент не выбран.

## <a name="cmfcribboncomboboxgetdropdownheight"></a><a name="getdropdownheight"></a> Кмфкриббонкомбобокс:: Жетдропдовнхеигхт

Возвращает высоту поля со списком при перетаскивании списка.

```cpp
int GetDropDownHeight();
```

### <a name="return-value"></a>Возвращаемое значение

Высота (в пикселях) поля со списком.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncomboboxgetintermediatesize"></a><a name="getintermediatesize"></a> Кмфкриббонкомбобокс:: GetIntermediateSize

Возвращает размер поля со списком, отображаемого в промежуточном режиме.

```cpp
virtual CSize GetIntermediateSize(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства для поля со списком.

### <a name="return-value"></a>Возвращаемое значение

Размер поля со списком.

### <a name="remarks"></a>Комментарии

Возвращаемый размер зависит от размера поля со списком при отображении мелких изображений.

## <a name="cmfcribboncomboboxgetitem"></a><a name="getitem"></a> Кмфкриббонкомбобокс:: DataItem

Возвращает строку, связанную с элементом по указанному индексу в поле со списком.

```cpp
LPCTSTR GetItem(int iIndex) const;
```

### <a name="parameters"></a>Параметры

*ииндекс*<br/>
окне Отсчитываемый от нуля индекс элемента в списке.

### <a name="return-value"></a>Возвращаемое значение

Указатель на строку, связанную с элементом; в противном случае значение NULL, если параметр индекса является недопустимым, или если параметр индекса имеет значение-1 и в поле со списком не выбран элемент.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncomboboxgetitemdata"></a><a name="getitemdata"></a> Кмфкриббонкомбобокс:: Жетитемдата

Возвращает данные, связанные с элементом по указанному индексу в списке.

```cpp
DWORD_PTR GetItemData(int iIndex) const;
```

### <a name="parameters"></a>Параметры

*ииндекс*<br/>
окне Отсчитываемый от нуля индекс элемента в списке.

### <a name="return-value"></a>Возвращаемое значение

Данные, связанные с элементом; значение 0, если элемент не существует, или значение, если параметр индекса равен-1 и в списке нет выделенного элемента.

## <a name="cmfcribboncomboboxhaseditbox"></a><a name="haseditbox"></a> Кмфкриббонкомбобокс:: Хаседитбокс

Указывает, содержит ли элемент управления поле ввода.

```cpp
BOOL HasEditBox() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если элемент управления содержит поле ввода; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncomboboxisresizedropdownlist"></a><a name="isresizedropdownlist"></a> Кмфкриббонкомбобокс:: Исресизедропдовнлист

Указывает, можно ли изменить размер окна списка.

```cpp
BOOL IsResizeDropDownList() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если можно изменить размер списка; в противном случае — FALSE. [Кмфкриббонкомбобокс:: Енабледропдовнлистресизе](#enabledropdownlistresize)

### <a name="remarks"></a>Комментарии

Можно включить изменение размера поля со списком с помощью метода [кмфкриббонкомбобокс:: енабледропдовнлистресизе](#enabledropdownlistresize) .

## <a name="cmfcribboncomboboxonselectitem"></a><a name="onselectitem"></a> Кмфкриббонкомбобокс:: Онселектитем

Вызывается платформой, когда пользователь выбирает элемент в списке.

```cpp
virtual void OnSelectItem(int nItem);
```

### <a name="parameters"></a>Параметры

*нитем*<br/>
окне Индекс выбранного элемента.

### <a name="remarks"></a>Комментарии

Переопределите этот метод, если требуется обработать входные данные пользователя.

## <a name="cmfcribboncomboboxremoveallitems"></a><a name="removeallitems"></a> Кмфкриббонкомбобокс:: Ремовеаллитемс

Удаляет все элементы из списка и очищает поле ввода.

```cpp
void RemoveAllItems();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncomboboxselectitem"></a><a name="selectitem"></a> Кмфкриббонкомбобокс:: Селектитем

Выбирает элемент в списке.

```cpp
BOOL SelectItem(int iIndex);
BOOL SelectItem(DWORD_PTR dwData);

BOOL SelectItem(LPCTSTR lpszText);
```

### <a name="parameters"></a>Параметры

*ииндекс*<br/>
окне Отсчитываемый от нуля индекс элемента в списке.

*двдата*<br/>
окне Данные, связанные с элементом в списке.

*lpszText*<br/>
окне Строка элемента в списке.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если метод выполнен успешно; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncomboboxsetdropdownheight"></a><a name="setdropdownheight"></a> Кмфкриббонкомбобокс:: Сетдропдовнхеигхт

Задает высоту поля со списком при его перетаскивании.

```cpp
void SetDropDownHeight(int nHeight);
```

### <a name="parameters"></a>Параметры

*нхеигхт*<br/>
окне Высота (в пикселях) поля со списком.

### <a name="remarks"></a>Комментарии

Высота по умолчанию — 150 пикселей.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md)
