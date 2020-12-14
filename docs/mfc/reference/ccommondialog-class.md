---
description: 'Дополнительные сведения о: Ккоммондиалог Class'
title: Класс Ккоммондиалог
ms.date: 11/04/2016
f1_keywords:
- CCommonDialog
- AFXDLGS/CCommonDialog
- AFXDLGS/CCommonDialog::CCommonDialog
helpviewer_keywords:
- CCommonDialog [MFC], CCommonDialog
ms.assetid: 1f68d65f-a0fd-4778-be22-ebbe51a95f95
ms.openlocfilehash: 927348982529f14eb0ad762019bb4463aaa77c99
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227901"
---
# <a name="ccommondialog-class"></a>Класс Ккоммондиалог

Базовый класс для классов, которые инкапсулируют функцию общих диалоговых окон Windows.

## <a name="syntax"></a>Синтаксис

```
class CCommonDialog : public CDialog
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккоммондиалог:: Ккоммондиалог](#ccommondialog)|Формирует объект `CCommonDialog`.|

## <a name="remarks"></a>Комментарии

Следующие классы инкапсулируют функциональные возможности общих диалоговых окон Windows:

- [CFileDialog](../../mfc/reference/cfiledialog-class.md)

- [CFontDialog](../../mfc/reference/cfontdialog-class.md)

- [CColorDialog](../../mfc/reference/ccolordialog-class.md)

- [CPageSetupDialog](../../mfc/reference/cpagesetupdialog-class.md)

- [CPrintDialog](../../mfc/reference/cprintdialog-class.md)

- [CPrintDialogEx](../../mfc/reference/cprintdialogex-class.md)

- [CFindReplaceDialog](../../mfc/reference/cfindreplacedialog-class.md)

- [COleDialog](../../mfc/reference/coledialog-class.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

`CCommonDialog`

## <a name="requirements"></a>Требования

**Заголовок:** афксдлгс. h

## <a name="ccommondialogccommondialog"></a><a name="ccommondialog"></a> Ккоммондиалог:: Ккоммондиалог

Формирует объект `CCommonDialog`.

```
explicit CCommonDialog(CWnd* pParentWnd);
```

### <a name="parameters"></a>Параметры

*ппарентвнд*<br/>
Указывает на родительский элемент или объект окна-владельца (типа [CWnd](../../mfc/reference/cwnd-class.md)), которому принадлежит объект диалогового окна. Если значение равно NULL, то родительское окно объекта диалогового окна устанавливается в главное окно приложения.

### <a name="remarks"></a>Комментарии

Полные сведения см. в разделе [CDialog:: CDialog](../../mfc/reference/cdialog-class.md#cdialog) .

## <a name="see-also"></a>См. также раздел

[Класс CDialog](../../mfc/reference/cdialog-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CFileDialog](../../mfc/reference/cfiledialog-class.md)<br/>
[Класс Кфонтдиалог](../../mfc/reference/cfontdialog-class.md)<br/>
[Класс Кколордиалог](../../mfc/reference/ccolordialog-class.md)<br/>
[Класс Кпажесетупдиалог](../../mfc/reference/cpagesetupdialog-class.md)<br/>
[Класс Кпринтдиалог](../../mfc/reference/cprintdialog-class.md)<br/>
[Класс диалоговое CFindReplaceDialog](../../mfc/reference/cfindreplacedialog-class.md)<br/>
[Класс Коледиалог](../../mfc/reference/coledialog-class.md)
