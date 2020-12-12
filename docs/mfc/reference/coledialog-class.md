---
description: 'Дополнительные сведения о: Коледиалог Class'
title: Класс Коледиалог
ms.date: 11/04/2016
f1_keywords:
- COleDialog
- AFXODLGS/COleDialog
- AFXODLGS/COleDialog::GetLastError
helpviewer_keywords:
- COleDialog [MFC], GetLastError
ms.assetid: b1ed0aca-3914-4b00-af34-4a4fb491aec7
ms.openlocfilehash: 9bdb532d58136ac2aac622fa88f674e60ec7221e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227303"
---
# <a name="coledialog-class"></a>Класс Коледиалог

Предоставляет стандартные функции для диалоговых окон OLE.

## <a name="syntax"></a>Синтаксис

```
class COleDialog : public CCommonDialog
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Коледиалог:: GetLastError](#getlasterror)|Возвращает код ошибки, возвращенный диалоговым окном.|

## <a name="remarks"></a>Комментарии

Библиотека Microsoft Foundation Class предоставляет несколько классов, производных от `COleDialog` :

- [COleInsertDialog](../../mfc/reference/coleinsertdialog-class.md)

- [COleConvertDialog](../../mfc/reference/coleconvertdialog-class.md)

- [COleChangeIconDialog](../../mfc/reference/colechangeicondialog-class.md)

- [COleLinksDialog](../../mfc/reference/colelinksdialog-class.md)

- [COleBusyDialog](../../mfc/reference/colebusydialog-class.md)

- [COleUpdateDialog](../../mfc/reference/coleupdatedialog-class.md)

- [COlePasteSpecialDialog](../../mfc/reference/colepastespecialdialog-class.md)

- [COlePropertiesDialog](../../mfc/reference/colepropertiesdialog-class.md)

- [COleChangeSourceDialog](../../mfc/reference/colechangesourcedialog-class.md)

Дополнительные сведения о диалоговых окнах, связанных с OLE, см. в разделе [диалоговые окна статьи в OLE](../../mfc/dialog-boxes-in-ole.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CCommonDialog](../../mfc/reference/ccommondialog-class.md)

`COleDialog`

## <a name="requirements"></a>Требования

**Заголовок:** афксодлгс. h

## <a name="coledialoggetlasterror"></a><a name="getlasterror"></a> Коледиалог:: GetLastError

Вызовите `GetLastError` функцию члена, чтобы получить дополнительные сведения об ошибке при `DoModal` возвращении идаборт.

```
UINT GetLastError() const;
```

### <a name="return-value"></a>Возвращаемое значение

Коды ошибок, возвращаемые, `GetLastError` зависят от отображаемого диалогового окна.

### <a name="remarks"></a>Комментарии

`DoModal`Сведения о конкретных сообщениях об ошибках см. в описании функции члена в производных классах.

## <a name="see-also"></a>См. также раздел

[Класс Ккоммондиалог](../../mfc/reference/ccommondialog-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
