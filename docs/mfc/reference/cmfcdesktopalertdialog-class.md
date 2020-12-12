---
description: 'Дополнительные сведения о: Кмфкдесктопалертдиалог Class'
title: Класс Кмфкдесктопалертдиалог
ms.date: 10/18/2018
f1_keywords:
- CMFCDesktopAlertDialog
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertDialog
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertDialog::CreateFromParams
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertDialog::GetDlgSize
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertDialog::HasFocus
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertDialog::PreTranslateMessage
helpviewer_keywords:
- CMFCDesktopAlertDialog [MFC], CreateFromParams
- CMFCDesktopAlertDialog [MFC], GetDlgSize
- CMFCDesktopAlertDialog [MFC], HasFocus
- CMFCDesktopAlertDialog [MFC], PreTranslateMessage
ms.assetid: a53c60aa-9607-485b-b826-ec64962075f6
ms.openlocfilehash: 327ec72b1e58d90e768f51c083ff9545f24f6f0b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193192"
---
# <a name="cmfcdesktopalertdialog-class"></a>Класс Кмфкдесктопалертдиалог

`CMFCDesktopAlertDialog`Класс используется вместе с [классом CMFCDesktopAlertWnd](../../mfc/reference/cmfcdesktopalertwnd-class.md) для вывода пользовательского диалогового окна во всплывающем окне.

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMFCDesktopAlertDialog : public CDialogEx
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCDesktopAlertDialog::CreateFromParams](#createfromparams)||
|[CMFCDesktopAlertDialog::GetDlgSize](#getdlgsize)||
|[CMFCDesktopAlertDialog::HasFocus](#hasfocus)||
|[CMFCDesktopAlertDialog::PreTranslateMessage](#pretranslatemessage)|(Переопределяет `CDialogEx::PreTranslateMessage`.)|

### <a name="remarks"></a>Комментарии

Чтобы отобразить настраиваемое диалоговое окно во всплывающем окне, выполните следующие действия:

1. Создайте производный класс от класса `CMFCDesktopAlertDialog`.

1. Создайте в ресурсах проекта шаблон дочернего диалогового окна.

1. Вызовите [CMFCDesktopAlertWnd:: Create](../../mfc/reference/cmfcdesktopalertwnd-class.md#create) с идентификатором ресурса шаблона диалогового окна и указателем на сведения о классе среды выполнения производного класса в качестве параметров.

1. Создайте настраиваемое диалоговое окно для обработки всех уведомлений, поступающих от размещенных элементов управления, или размещенные элементы управления для обработки этих уведомлений напрямую.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CDialogEx](../../mfc/reference/cdialogex-class.md)

[CMFCDesktopAlertDialog](../../mfc/reference/cmfcdesktopalertdialog-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксдесктопалертдиалог. h

## <a name="cmfcdesktopalertdialogcreatefromparams"></a><a name="createfromparams"></a> Кмфкдесктопалертдиалог:: Креатефромпарамс

```
BOOL CreateFromParams(
    CMFCDesktopAlertWndInfo& params,
    CMFCDesktopAlertWnd* pParent);
```

### <a name="parameters"></a>Параметры

окне *Параметры*<br/>

окне *ппарент*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertdialoggetdlgsize"></a><a name="getdlgsize"></a> Кмфкдесктопалертдиалог:: Жетдлгсизе

```
CSize GetDlgSize();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertdialoghasfocus"></a><a name="hasfocus"></a> Кмфкдесктопалертдиалог:: Хасфокус

```
BOOL HasFocus() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertdialogpretranslatemessage"></a><a name="pretranslatemessage"></a> Кмфкдесктопалертдиалог::P Ретранслатемессаже

```
virtual BOOL PreTranslateMessage(MSG* pMsg);
```

### <a name="parameters"></a>Параметры

[in] *pMsg*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCDesktopAlertWnd](../../mfc/reference/cmfcdesktopalertwnd-class.md)<br/>
[Класс Кмфкдесктопалертвндинфо](../../mfc/reference/cmfcdesktopalertwndinfo-class.md)<br/>
[Класс Кдиаложекс](../../mfc/reference/cdialogex-class.md)
