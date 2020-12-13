---
description: 'Дополнительные сведения о: Кмфкспинбуттонктрл Class'
title: Класс Кмфкспинбуттонктрл
ms.date: 11/04/2016
f1_keywords:
- CMFCSpinButtonCtrl
- AFXSPINBUTTONCTRL/CMFCSpinButtonCtrl
- AFXSPINBUTTONCTRL/CMFCSpinButtonCtrl::OnDraw
helpviewer_keywords:
- CMFCSpinButtonCtrl [MFC], OnDraw
ms.assetid: 8773f259-4d3f-4bca-a71c-09e0c71bc843
ms.openlocfilehash: 87e9abc94247416704ab801beeaa1953c4cceb46
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339643"
---
# <a name="cmfcspinbuttonctrl-class"></a>Класс Кмфкспинбуттонктрл

`CMFCSpinButtonCtrl`Класс поддерживает визуальный диспетчер, который рисует элемент управления "Счетчик".

## <a name="syntax"></a>Синтаксис

```
class CMFCSpinButtonCtrl : public CSpinButtonCtrl
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCSpinButtonCtrl::CMFCSpinButtonCtrl`|Конструктор по умолчанию.|
|`CMFCSpinButtonCtrl::~CMFCSpinButtonCtrl`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкспинбуттонктрл:: OnDraw](#ondraw)|Перерисовывает текущий элемент управления "Счетчик".|

## <a name="remarks"></a>Комментарии

Чтобы использовать визуальный диспетчер для рисования элемента управления "Счетчик" в приложении, замените все экземпляры `CSpinButtonCtrl` класса `CMFCSpinButtonCtrl` классом.

## <a name="example"></a>Пример

В следующем примере показано, как создать объект `CMFCSpinButtonCtrl` класса и использовать его `Create` метод.

[!code-cpp[NVC_MFC_RibbonApp#25](../../mfc/reference/codesnippet/cpp/cmfcspinbuttonctrl-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CSpinButtonCtrl](../../mfc/reference/cspinbuttonctrl-class.md)

[CMFCSpinButtonCtrl](../../mfc/reference/cmfcspinbuttonctrl-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксспинбуттонктрл. h

## <a name="cmfcspinbuttonctrlondraw"></a><a name="ondraw"></a> Кмфкспинбуттонктрл:: OnDraw

Перерисовывает текущий элемент управления "Счетчик".

```
virtual void OnDraw(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

### <a name="remarks"></a>Комментарии

Платформа вызывает `CMFCSpinButtonCtrl::OnPaint` метод для работы с сообщением [CWnd:: onpain](../../mfc/reference/cwnd-class.md#onpaint) , а этот метод, в свою очередь, вызывает этот `CMFCSpinButtonCtrl::OnDraw` метод. Переопределите этот метод, чтобы настроить способ, которым платформа рисует элемент управления "Счетчик".

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCVisualManager](../../mfc/reference/cmfcvisualmanager-class.md)
