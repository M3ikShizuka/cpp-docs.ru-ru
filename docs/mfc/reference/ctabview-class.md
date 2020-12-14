---
description: 'Дополнительные сведения о: Ктабвиев Class'
title: Класс Ктабвиев
ms.date: 11/04/2016
f1_keywords:
- CTabView
- AFXTABVIEW/CTabView
- AFXTABVIEW/CTabView::AddView
- AFXTABVIEW/CTabView::FindTab
- AFXTABVIEW/CTabView::GetActiveView
- AFXTABVIEW/CTabView::GetTabControl
- AFXTABVIEW/CTabView::RemoveView
- AFXTABVIEW/CTabView::SetActiveView
- AFXTABVIEW/CTabView::IsScrollBar
- AFXTABVIEW/CTabView::OnActivateView
helpviewer_keywords:
- CTabView [MFC], AddView
- CTabView [MFC], FindTab
- CTabView [MFC], GetActiveView
- CTabView [MFC], GetTabControl
- CTabView [MFC], RemoveView
- CTabView [MFC], SetActiveView
- CTabView [MFC], IsScrollBar
- CTabView [MFC], OnActivateView
ms.assetid: 8e6ecd9d-d28d-432b-8ec8-0446f0204d52
ms.openlocfilehash: 59d4169bae108575fcf4844ec7c5c6e1e6681e28
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97345060"
---
# <a name="ctabview-class"></a>Класс Ктабвиев

`CTabView`Класс упрощает использование класса элемента управления Tab ( [CMFCTabCtrl](../../mfc/reference/ctabview-class.md)) в приложениях, использующих архитектуру документов и представлений MFC.

## <a name="syntax"></a>Синтаксис

```
class CTabbedView : public CView
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ктабвиев:: Аддвиев](#addview)|Добавляет новое представление в элемент управления "Вкладка".|
|[Ктабвиев:: Финдтаб](#findtab)|Возвращает индекс указанного представления в элементе управления "Вкладка".|
|[Ктабвиев:: Жетактивевиев](#getactiveview)|Возвращает указатель на текущее активное представление|
|[Ктабвиев::, TabControl](#gettabcontrol)|Возвращает ссылку на элемент управления Tab, связанный с представлением.|
|[Ктабвиев:: Ремовевиев](#removeview)|Удаляет представление из элемента управления "Вкладка".|
|[Ктабвиев:: Сетактивевиев](#setactiveview)|Делает представление активным.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Ктабвиев:: ScrollBar](#isscrollbar)|Вызывается структурой при создании представления вкладки, чтобы определить, имеет ли представление вкладки общую горизонтальную полосу прокрутки.|
|[Ктабвиев:: Онактиватевиев](#onactivateview)|Вызывается структурой, когда представление вкладки становится активным или неактивным.|

## <a name="remarks"></a>Комментарии

Этот класс упрощает помещение представления с вкладками в приложение "документ/представление". `CTabView` является `CView` производным классом, который содержит внедренный `CMFCTabCtrl` объект. `CTabView` обрабатывает все сообщения, необходимые для поддержки `CMFCTabCtrl` объекта. Просто создайте производный класс от `CTabView` и подключите его к приложению, а затем добавьте классы, производные от класса, с `CView` помощью `AddView` метода. Элемент управления "Вкладка" будет отображать эти представления в виде вкладок.

Например, документ может быть представлен различными способами: в виде электронной таблицы, диаграммы, редактируемой формы и т. д. Можно создать отдельные представления для отображения данных по мере необходимости, вставить их в `CTabView` объект, производный от, и сделать их без дополнительного программирования.

[Пример таббедвиев. приложение MFC с вкладками Просмотр](../../overview/visual-cpp-samples.md) демонстрирует использование `CTabView` .

## <a name="example"></a>Пример

В следующем примере показано, как `CTabView` используется в образце таббедвиев.

[!code-cpp[NVC_MFC_TabbedView#1](../../mfc/reference/codesnippet/cpp/ctabview-class_1.h)]

## <a name="requirements"></a>Требования

**Заголовок:** афкстабвиев. h

## <a name="ctabviewaddview"></a><a name="addview"></a> Ктабвиев:: Аддвиев

Добавляет представление в элемент управления "Вкладка".

```
int AddView(
    CRuntimeClass* pViewClass,
    const CString& strViewLabel,
    int iIndex=-1,
    CCreateContext* pContext=NULL);
```

### <a name="parameters"></a>Параметры

*пвиевкласс*<br/>
окне Указатель на класс среды выполнения вставленного представления.

*стрвиевлабел*<br/>
окне Задает текст вкладки.

*ииндекс*<br/>
окне Задает отсчитываемый от нуля индекс места вставки представления. Если позиции равно-1, в конце вставляется новая вкладка.

*pContext*<br/>
окне Указатель на объект `CCreateContext` представления.

### <a name="return-value"></a>Возвращаемое значение

Индекс представления, если этот метод завершился с ошибкой. В противном случае –1.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы добавить представление в элемент управления "Вкладка", внедренный в кадр.

## <a name="ctabviewfindtab"></a><a name="findtab"></a> Ктабвиев:: Финдтаб

Возвращает индекс указанного представления в элементе управления "Вкладка".

```
int FindTab(HWND hWndView) const;
```

### <a name="parameters"></a>Параметры

*хвндвиев*<br/>
окне Маркер представления.

### <a name="return-value"></a>Возвращаемое значение

Индекс представления, если он найден; в противном случае — значение-1.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить индекс представления с указанным маркером.

## <a name="ctabviewgetactiveview"></a><a name="getactiveview"></a> Ктабвиев:: Жетактивевиев

Возвращает указатель на текущее активное представление.

```
CView* GetActiveView() const;
```

### <a name="return-value"></a>Возвращаемое значение

Допустимый указатель на активное представление или значение NULL, если активное представление отсутствует.

### <a name="remarks"></a>Комментарии

## <a name="ctabviewgettabcontrol"></a><a name="gettabcontrol"></a> Ктабвиев::, TabControl

Возвращает ссылку на элемент управления Tab, связанный с представлением.

```
DECLARE_DYNCREATE CMFCTabCtrl& GetTabControl();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на элемент управления Tab, связанный с представлением.

## <a name="ctabviewisscrollbar"></a><a name="isscrollbar"></a> Ктабвиев:: ScrollBar

Вызывается структурой при создании представления вкладки, чтобы определить, имеет ли представление вкладки общую горизонтальную полосу прокрутки.

```
virtual BOOL IsScrollBar() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если представление вкладки должно создаваться вместе с общей полосой прокрутки. В противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Платформа вызывает этот метод при создании объекта *ктабвиев* .

Переопределите *метод* *ктабвиев* в классе, производном от класса, и возвратите значение true, если требуется создать представление с общей горизонтальной полосой прокрутки.

## <a name="ctabviewonactivateview"></a><a name="onactivateview"></a> Ктабвиев:: Онактиватевиев

Вызывается структурой, когда представление вкладки становится активным или неактивным.

```
virtual void OnActivateView(CView* view);
```

### <a name="parameters"></a>Параметры

*view*<br/>
окне Указатель на представление.

### <a name="remarks"></a>Комментарии

Реализация по умолчанию не выполняет никаких действий. Переопределите этот метод в `CTabView` классе, производном от, чтобы обработать это уведомление.

## <a name="ctabviewremoveview"></a><a name="removeview"></a> Ктабвиев:: Ремовевиев

Удаляет представление из элемента управления "Вкладка".

```
BOOL RemoveView(int iTabNum);
```

### <a name="parameters"></a>Параметры

*iTabNum*<br/>
окне Индекс удаляемого представления.

### <a name="return-value"></a>Возвращаемое значение

Индекс удаленного представления, если этот метод завершился с ошибкой. В противном случае — 1.

### <a name="remarks"></a>Комментарии

## <a name="ctabviewsetactiveview"></a><a name="setactiveview"></a> Ктабвиев:: Сетактивевиев

Делает представление активным.

```
BOOL SetActiveView(int iTabNum);
```

### <a name="parameters"></a>Параметры

*iTabNum*<br/>
окне Отсчитываемый от нуля индекс представления вкладки.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если указанное представление было активно, и FALSE, если индекс представления является недопустимым.

### <a name="remarks"></a>Комментарии

Дополнительные сведения см. в разделе [CMFCTabCtrl:: сетактиветаб](../../mfc/reference/cmfctabctrl-class.md#setactivetab).

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[CMFCTabCtrl](../../mfc/reference/ctabview-class.md)<br/>
[Класс CView](../../mfc/reference/cview-class.md)
