---
description: 'Дополнительные сведения о: CFolderPickerDialog Class'
title: Класс CFolderPickerDialog
ms.date: 03/27/2019
f1_keywords:
- CFolderPickerDialog
- AFXDLGS/CFolderPickerDialog
- AFXDLGS/CFolderPickerDialog::CFolderPickerDialog
helpviewer_keywords:
- CFolderPickerDialog [MFC], CFolderPickerDialog
ms.assetid: 8db01684-dd1d-4e9c-989e-07a2318a8156
ms.openlocfilehash: f4a5bcc3162a5fffcc723d7ec420685b02be10f0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97184430"
---
# <a name="cfolderpickerdialog-class"></a>Класс CFolderPickerDialog

Класс CFolderPickerDialog реализует CFileDialog в режиме выбора папки.

## <a name="syntax"></a>Синтаксис

```
class CFolderPickerDialog : public CFileDialog;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CFolderPickerDialog:: ~ CFolderPickerDialog](#_dtorcfolderpickerdialog)|Деструктор.|
|[CFolderPickerDialog:: CFolderPickerDialog](#cfolderpickerdialog)|Конструктор.|

## <a name="remarks"></a>Комментарии

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CCommonDialog](../../mfc/reference/ccommondialog-class.md)

[CFileDialog](../../mfc/reference/cfiledialog-class.md)

`CFolderPickerDialog`

## <a name="requirements"></a>Требования

**Заголовок:** афксдлгс. h

## <a name="cfolderpickerdialogcfolderpickerdialog"></a><a name="cfolderpickerdialog"></a> CFolderPickerDialog:: CFolderPickerDialog

Конструктор.

```
explicit CFolderPickerDialog(
    LPCTSTR lpszFolder = NULL,
    DWORD dwFlags = 0,
    CWnd* pParentWnd = NULL,
    DWORD dwSize = 0);
```

### <a name="parameters"></a>Параметры

*лпсзфолдер*<br/>
Начальная папка.

*dwFlags*<br/>
Сочетание одного или нескольких флагов, которые позволяют настроить диалоговое окно.

*ппарентвнд*<br/>
Указатель на родительский узел или окно-владелец объекта диалогового окна.

*двсизе*<br/>
Размер структуры OPENFILENAME.

### <a name="remarks"></a>Комментарии

## <a name="cfolderpickerdialogcfolderpickerdialog"></a><a name="_dtorcfolderpickerdialog"></a> CFolderPickerDialog:: ~ CFolderPickerDialog

Деструктор.

```
virtual ~CFolderPickerDialog();
```

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
