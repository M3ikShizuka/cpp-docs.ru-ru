---
description: 'Дополнительные сведения о: CMFCRibbonButtonsGroup Class'
title: Класс CMFCRibbonButtonsGroup
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonButtonsGroup
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::CMFCRibbonButtonsGroup
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::AddButton
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::AddButtons
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::GetButton
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::GetCount
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::GetImageSize
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::GetRegularSize
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::HasImages
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::OnDrawImage
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::RemoveAll
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::SetImages
- AFXRIBBONBUTTONSGROUP/CMFCRibbonButtonsGroup::SetParentCategory
helpviewer_keywords:
- CMFCRibbonButtonsGroup [MFC], CMFCRibbonButtonsGroup
- CMFCRibbonButtonsGroup [MFC], AddButton
- CMFCRibbonButtonsGroup [MFC], AddButtons
- CMFCRibbonButtonsGroup [MFC], GetButton
- CMFCRibbonButtonsGroup [MFC], GetCount
- CMFCRibbonButtonsGroup [MFC], GetImageSize
- CMFCRibbonButtonsGroup [MFC], GetRegularSize
- CMFCRibbonButtonsGroup [MFC], HasImages
- CMFCRibbonButtonsGroup [MFC], OnDrawImage
- CMFCRibbonButtonsGroup [MFC], RemoveAll
- CMFCRibbonButtonsGroup [MFC], SetImages
- CMFCRibbonButtonsGroup [MFC], SetParentCategory
ms.assetid: b993d93e-fc1a-472f-a87f-1d7b7b499845
ms.openlocfilehash: 0b86ce6ff21bd36daaac9d68ce511ae395141170
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97293836"
---
# <a name="cmfcribbonbuttonsgroup-class"></a>Класс CMFCRibbonButtonsGroup

`CMFCRibbonButtonsGroup`Класс позволяет организовать набор кнопок ленты в группу. Все кнопки в группе располагаются непосредственно рядом с друг с другом по горизонтали и заключены в границу.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonButtonsGroup : public CMFCRibbonBaseElement
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonButtonsGroup::CMFCRibbonButtonsGroup](#cmfcribbonbuttonsgroup)|Формирует объект `CMFCRibbonButtonsGroup`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonButtonsGroup:: AddButton](#addbutton)|Добавляет кнопку в группу.|
|[CMFCRibbonButtonsGroup:: Аддбуттонс](#addbuttons)|Добавляет список кнопок в группу.|
|[CMFCRibbonButtonsGroup:: "Кнопка"](#getbutton)|Возвращает указатель на кнопку, расположенную по указанному индексу.|
|[CMFCRibbonButtonsGroup:: NOCOUNT](#getcount)|Возвращает число кнопок в группе.|
|[CMFCRibbonButtonsGroup::GetImageSize](#getimagesize)|Возвращает размер изображения обычных изображений в группе ленты (переопределяет [метод CMFCRibbonBaseElement:: жетимажесизе](../../mfc/reference/cmfcribbonbaseelement-class.md#getimagesize).)|
|[CMFCRibbonButtonsGroup::GetRegularSize](#getregularsize)|Возвращает обычный размер элемента ленты (переопределяет [метод CMFCRibbonBaseElement:: жетрегуларсизе](../../mfc/reference/cmfcribbonbaseelement-class.md#getregularsize).)|
|[CMFCRibbonButtonsGroup::HasImages](#hasimages)|Сообщает, `CMFCRibbonButtonsGroup` содержит ли объект изображения панели инструментов.|
|[CMFCRibbonButtonsGroup::OnDrawImage](#ondrawimage)|Рисует соответствующий рисунок для указанной кнопки в зависимости от того, является ли кнопка нормальной, выделенной или отключенной.|
|[CMFCRibbonButtonsGroup::RemoveAll](#removeall)|Удаляет все кнопки из `CMFCRibbonButtonsGroup` объекта.|
|[CMFCRibbonButtonsGroup:: Сетимажес](#setimages)|Назначает образы группе.|
|[CMFCRibbonButtonsGroup::SetParentCategory](#setparentcategory)|Задает родительский `CMFCRibbonCategory` объект для `CMFCRibbonButtonsGroup` объекта и все кнопки внутри него (переопределяет [метод CMFCRibbonBaseElement:: сетпаренткатегори](../../mfc/reference/cmfcribbonbaseelement-class.md#setparentcategory).)|

## <a name="remarks"></a>Комментарии

Группа является производной от [кмфкбасериббонелемент](../../mfc/reference/cmfcribbonbaseelement-class.md) и может управляться как единая сущность. Группу можно разместить на любой панели или в контекстном меню.

## <a name="example"></a>Пример

В приведенном ниже примере демонстрируется использование различных методов класса `CMFCRibbonButtonsGroup` . В примере показано, как создать `CMFCRibbonButtonsGroup` объект, назначить изображения группе кнопок ленты и добавить кнопку в группу кнопок ленты. Этот фрагмент кода входит в состав [примера Draw Client](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_DrawClient#2](../../mfc/reference/codesnippet/cpp/cmfcribbonbuttonsgroup-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonButtonsGroup](../../mfc/reference/cmfcribbonbuttonsgroup-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонбуттонсграуп. h

## <a name="cmfcribbonbuttonsgroupaddbutton"></a><a name="addbutton"></a> CMFCRibbonButtonsGroup:: AddButton

Добавляет кнопку в группу.

```cpp
void AddButton(CMFCRibbonBaseElement* pButton);
```

### <a name="parameters"></a>Параметры

*пбуттон*<br/>
окне Указатель на добавляемую кнопку.

## <a name="cmfcribbonbuttonsgroupaddbuttons"></a><a name="addbuttons"></a> CMFCRibbonButtonsGroup:: Аддбуттонс

Добавляет список кнопок в группу.

```cpp
void AddButtons(
    const CList<CMFCRibbonBaseElement*,CMFCRibbonBaseElement*>& lstButtons);
```

### <a name="parameters"></a>Параметры

*лстбуттонс*<br/>
окне Список указателей на кнопки, которые требуется добавить.

## <a name="cmfcribbonbuttonsgroupcmfcribbonbuttonsgroup"></a><a name="cmfcribbonbuttonsgroup"></a> CMFCRibbonButtonsGroup:: CMFCRibbonButtonsGroup

Формирует объект `CMFCRibbonButtonsGroup`.

```
CMFCRibbonButtonsGroup();
CMFCRibbonButtonsGroup(CMFCRibbonBaseElement* pButton);
```

### <a name="parameters"></a>Параметры

*пбуттон*<br/>
окне Задает кнопку, добавляемую к вновь созданному `CMFCRibbonButtonsGroup` объекту.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonbuttonsgroupgetbutton"></a><a name="getbutton"></a> CMFCRibbonButtonsGroup:: "Кнопка"

Возвращает указатель на кнопку, расположенную по указанному индексу.

```
CMFCRibbonBaseElement* GetButton(int i) const;
```

### <a name="parameters"></a>Параметры

*i*<br/>
окне Отсчитываемый от нуля индекс возвращаемой кнопки.

### <a name="return-value"></a>Возвращаемое значение

Указатель на кнопку, расположенную по указанному индексу. Значение NULL, если указанный индекс выходит за пределы допустимого диапазона.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonbuttonsgroupgetcount"></a><a name="getcount"></a> CMFCRibbonButtonsGroup:: NOCOUNT

Возвращает число кнопок в группе.

```
int GetCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число кнопок в группе.

## <a name="cmfcribbonbuttonsgroupgetimagesize"></a><a name="getimagesize"></a> CMFCRibbonButtonsGroup:: Жетимажесизе

Извлекает размер исходного изображения защищенного `CMFCToolBarImages` элемента `m_Images` .

```
const CSize GetImageSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает размер исходного изображения для изображений панели инструментов, если таковые имеются, или нуль, `CSize` Если нет.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonbuttonsgroupgetregularsize"></a><a name="getregularsize"></a> CMFCRibbonButtonsGroup:: Жетрегуларсизе

Возвращает максимальный возможный размер элемента группы ленты.

```
virtual CSize GetRegularSize(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства группы лент.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonbuttonsgrouphasimages"></a><a name="hasimages"></a> CMFCRibbonButtonsGroup:: Хасимажес

Сообщает, `CMFCRibbonButtonsGroup` содержит ли объект изображения панели инструментов.

```
BOOL HasImages() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если защищенный `CMFCToolBarImages` элемент `m_Images` содержит изображения, или значение false в противном случае.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonbuttonsgroupondrawimage"></a><a name="ondrawimage"></a> CMFCRibbonButtonsGroup:: Ондравимаже

Рисует соответствующий рисунок для указанной кнопки в зависимости от того, является ли кнопка нормальной, выделенной или отключенной.

```
virtual void OnDrawImage(
    CDC* pDC,
    CRect rectImage,
    CMFCRibbonBaseElement* pButton,
    int nImageIndex);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства `CMFCRibbonButtonsGroup` объекта.

*ректимаже*<br/>
окне Прямоугольник, в котором рисуется изображение.

*пбуттон*<br/>
окне Кнопка, для которой нарисовывается изображение.

*нимажеиндекс*<br/>
окне Индекс изображения, которое будет нарисовано на кнопке (в одном из трех массивов изображений для обычных, выделенных или отключенных кнопок).

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonbuttonsgroupremoveall"></a><a name="removeall"></a> CMFCRibbonButtonsGroup:: RemoveAll

Удаляет все кнопки из `CMFCRibbonButtonsGroup` объекта.

```cpp
void RemoveAll();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonbuttonsgroupsetimages"></a><a name="setimages"></a> CMFCRibbonButtonsGroup:: Сетимажес

Назначает изображения группе кнопок ленты.

```cpp
void SetImages(
    CMFCToolBarImages* pImages,
    CMFCToolBarImages* pHotImages,
    CMFCToolBarImages* pDisabledImages);
```

### <a name="parameters"></a>Параметры

*пимажес*<br/>
окне Обычные образы.

*фотимажес*<br/>
окне Горячие образы.

*пдисабледимажес*<br/>
окне Отключенные образы.

### <a name="remarks"></a>Комментарии

Вызовите, `SetImages` прежде чем добавлять кнопки в группу. Число образов должно быть больше или равно числу кнопок, добавляемых в группу.

> [!NOTE]
> Горячие образы — это изображения, которые отображаются, когда пользователь наводит указатель мыши на кнопку. Отключенные изображения — это изображения, отображаемые при отключенной кнопке.

## <a name="cmfcribbonbuttonsgroupsetparentcategory"></a><a name="setparentcategory"></a> CMFCRibbonButtonsGroup:: Сетпаренткатегори

Задает родительский `CMFCRibbonCategory` объект для `CMFCRibbonButtonsGroup` объекта и все кнопки внутри него.

```
virtual void SetParentCategory(CMFCRibbonCategory* pCategory);
```

### <a name="parameters"></a>Параметры

*пкатегори*<br/>
окне Указатель на родительскую категорию для установки (группы с вкладками в элементах управления ленты называются категориями).

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)
