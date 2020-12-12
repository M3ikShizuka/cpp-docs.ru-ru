---
description: 'Дополнительные сведения о: Кмфктулбаркомбобокседит Class'
title: Класс Кмфктулбаркомбобокседит
ms.date: 11/04/2016
f1_keywords:
- CMFCToolBarComboBoxEdit
- AFXTOOLBARCOMBOBOXBUTTON/CMFCToolBarComboBoxEdit
- AFXTOOLBARCOMBOBOXBUTTON/CMFCToolBarComboBoxEdit::CMFCToolBarComboBoxEdit
helpviewer_keywords:
- CMFCToolBarComboBoxEdit [MFC], CMFCToolBarComboBoxEdit
ms.assetid: 4789c34a-ce58-48ba-a26f-38748b601352
ms.openlocfilehash: f5b54c8c9eb13baf335c52074b1f529bb4f9dab7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97143472"
---
# <a name="cmfctoolbarcomboboxedit-class"></a>Класс Кмфктулбаркомбобокседит

Платформа использует `CMFCToolBarComboBoxEdit` класс для создания кнопки на панели инструментов, которая ведет себя как редактируемый элемент управления "поле со списком".

## <a name="syntax"></a>Синтаксис

```
class CMFCToolBarComboBoxEdit : public CEdit
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфктулбаркомбобокседит:: Кмфктулбаркомбобокседит](#cmfctoolbarcomboboxedit)|Формирует объект `CMFCToolBarComboBoxEdit`.|
|`CMFCToolBarComboBoxEdit::~CMFCToolBarComboBoxEdit`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|`CMFCToolBarComboBoxEdit::PreTranslateMessage`|Преобразует сообщения окна до их отправки в функции Windows [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage) и [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) . (Переопределяет [CWnd::PreTranslateMessage](../../mfc/reference/cwnd-class.md#pretranslatemessage).)|

### <a name="remarks"></a>Комментарии

Создайте класс, производный от `CMFCToolBarComboBoxEdit` класса, для настройки его операций изменения.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CEdit](../../mfc/reference/cedit-class.md)

[CMFCToolBarComboBoxEdit](../../mfc/reference/cmfctoolbarcomboboxedit-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкстулбаркомбобоксбуттон. h

## <a name="cmfctoolbarcomboboxeditcmfctoolbarcomboboxedit"></a><a name="cmfctoolbarcomboboxedit"></a> Кмфктулбаркомбобокседит:: Кмфктулбаркомбобокседит

Формирует объект `CMFCToolBarComboBoxEdit`.

```
CMFCToolBarComboBoxEdit(CMFCToolBarComboBoxButton& combo);
```

### <a name="parameters"></a>Параметры

*поле*<br/>
окне Ссылка на объект [кмфктулбаркомбобоксбуттон](../../mfc/reference/cmfctoolbarcomboboxbutton-class.md) , который является кнопкой панели инструментов, содержащей элемент управления "поле со списком".

### <a name="example"></a>Пример

В следующем примере показано, как создать объект `CMFCToolBarComboBoxEdit` класса. Этот фрагмент кода является частью [примера демонстрационной версии IE](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_IEDemo#5](../../mfc/reference/codesnippet/cpp/cmfctoolbarcomboboxedit-class_1.cpp)]

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфктулбаркомбобоксбуттон](../../mfc/reference/cmfctoolbarcomboboxbutton-class.md)
