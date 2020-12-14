---
description: 'Дополнительные сведения о: Колелинксдиалог Class'
title: Класс Колелинксдиалог
ms.date: 11/04/2016
f1_keywords:
- COleLinksDialog
- AFXODLGS/COleLinksDialog
- AFXODLGS/COleLinksDialog::COleLinksDialog
- AFXODLGS/COleLinksDialog::DoModal
- AFXODLGS/COleLinksDialog::m_el
helpviewer_keywords:
- COleLinksDialog [MFC], COleLinksDialog
- COleLinksDialog [MFC], DoModal
- COleLinksDialog [MFC], m_el
ms.assetid: fb2eb638-2809-46db-ac74-392a732affc7
ms.openlocfilehash: 036fc2b97fe4ad529e87c3573e280c99ac157848
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226926"
---
# <a name="colelinksdialog-class"></a>Класс Колелинксдиалог

Используется для диалогового окна OLE "Изменить ссылки".

## <a name="syntax"></a>Синтаксис

```
class COleLinksDialog : public COleDialog
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Колелинксдиалог:: Колелинксдиалог](#colelinksdialog)|Формирует объект `COleLinksDialog`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Колелинксдиалог::D Омодал](#domodal)|Отображает диалоговое окно «Редактирование ссылок OLE».|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[COleLinksDialog::m_el](#m_el)|Структура типа ОЛЕУИЕДИТЛИНКС, которая управляет поведением диалогового окна.|

## <a name="remarks"></a>Комментарии

Создайте объект класса, `COleLinksDialog` Если нужно вызвать это диалоговое окно. После создания `COleLinksDialog` объекта можно использовать структуру [m_el](#m_el) для инициализации значений или состояний элементов управления в диалоговом окне. `m_el`Структура имеет тип олеуиедитлинкс. Дополнительные сведения об использовании этого класса диалогового окна см. в описании функции члена [DoModal](#domodal) .

> [!NOTE]
> Созданный мастером приложений код контейнера использует этот класс.

Дополнительные сведения см. в описании структуры [олеуиедитлинкс](/windows/win32/api/oledlg/ns-oledlg-oleuieditlinksw) в Windows SDK.

Дополнительные сведения о диалоговых окнах, связанных с OLE, см. в разделе [диалоговые окна статьи в OLE](../../mfc/dialog-boxes-in-ole.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CCommonDialog](../../mfc/reference/ccommondialog-class.md)

[COleDialog](../../mfc/reference/coledialog-class.md)

`COleLinksDialog`

## <a name="requirements"></a>Требования

**Заголовок:** афксодлгс. h

## <a name="colelinksdialogdomodal"></a><a name="domodal"></a> Колелинксдиалог::D Омодал

Отображает диалоговое окно «Редактирование ссылок OLE».

```
virtual INT_PTR DoModal();
```

### <a name="return-value"></a>Возвращаемое значение

Состояние завершения для диалогового окна. Одно из следующих значений:

- ИДОК, если диалоговое окно было успешно отображено.

- ИДКАНЦЕЛ, если пользователь отменил диалоговое окно.

- ИДАБОРТ, если произошла ошибка. Если возвращается ИДАБОРТ, вызовите `COleDialog::GetLastError` функцию-член, чтобы получить дополнительные сведения о типе произошедшей ошибки. Список возможных ошибок см. в описании функции [олеуиедитлинкс](/windows/win32/api/oledlg/nf-oledlg-oleuieditlinksw) в Windows SDK.

### <a name="remarks"></a>Комментарии

Если требуется инициализировать различные элементы управления диалогового окна путем установки элементов структуры [m_el](#m_el) , следует выполнить их перед вызовом метода `DoModal` , но после создания объекта диалогового окна.

## <a name="colelinksdialogcolelinksdialog"></a><a name="colelinksdialog"></a> Колелинксдиалог:: Колелинксдиалог

Формирует объект `COleLinksDialog`.

```
COleLinksDialog (
    COleDocument* pDoc,
    CView* pView,
    DWORD dwFlags = 0,
    CWnd* pParentWnd = NULL);
```

### <a name="parameters"></a>Параметры

*pDoc*<br/>
Указывает на документ OLE, содержащий ссылки для изменения.

*pView*<br/>
Указывает на текущее представление в *pDoc*.

*dwFlags*<br/>
Флаг создания, который содержит 0 или ELF_SHOWHELP, чтобы указать, будет ли отображаться кнопка "Справка" при отображении диалогового окна.

*ппарентвнд*<br/>
Указывает на родительский элемент или объект окна-владельца (типа `CWnd` ), которому принадлежит объект диалогового окна. Если это значение равно NULL, родительскому окну диалогового окна присваивается основное окно приложения.

### <a name="remarks"></a>Комментарии

Эта функция конструирует только `COleLinksDialog` объект. Чтобы открыть диалоговое окно, вызовите функцию [DoModal](#domodal) .

## <a name="colelinksdialogm_el"></a><a name="m_el"></a> Колелинксдиалог:: m_el

Структура типа ОЛЕУИЕДИТЛИНКС, используемая для управления поведением диалогового окна "изменение ссылок".

```
OLEUIEDITLINKS m_el;
```

### <a name="remarks"></a>Комментарии

Члены этой структуры можно изменять напрямую или с помощью функций-членов.

Дополнительные сведения см. в описании структуры [олеуиедитлинкс](/windows/win32/api/oledlg/ns-oledlg-oleuieditlinksw) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Класс Коледиалог](../../mfc/reference/coledialog-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Коледиалог](../../mfc/reference/coledialog-class.md)
