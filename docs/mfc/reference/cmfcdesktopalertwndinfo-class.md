---
description: 'Дополнительные сведения о: Кмфкдесктопалертвндинфо Class'
title: Класс Кмфкдесктопалертвндинфо
ms.date: 10/18/2018
f1_keywords:
- CMFCDesktopAlertWndInfo
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertWndInfo
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertWndInfo::m_hIcon
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertWndInfo::m_nURLCmdID
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertWndInfo::m_strText
- AFXDESKTOPALERTDIALOG/CMFCDesktopAlertWndInfo::m_strURL
helpviewer_keywords:
- CMFCDesktopAlertWndInfo [MFC], m_hIcon
- CMFCDesktopAlertWndInfo [MFC], m_nURLCmdID
- CMFCDesktopAlertWndInfo [MFC], m_strText
- CMFCDesktopAlertWndInfo [MFC], m_strURL
ms.assetid: 5c9bb84e-6c96-4748-8e74-6951b6ae8e84
ms.openlocfilehash: 1c23e5b890e892df9bccce51542f2d36b3d6f7d4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97250690"
---
# <a name="cmfcdesktopalertwndinfo-class"></a>Класс Кмфкдесктопалертвндинфо

`CMFCDesktopAlertWndInfo`Класс используется с [классом CMFCDesktopAlertWnd](../../mfc/reference/cmfcdesktopalertwnd-class.md). Определяет элементы управления, которые отображаются, если всплывает окно оповещения.

## <a name="syntax"></a>Синтаксис

```
class CMFCDesktopAlertWndInfo
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCDesktopAlertWndInfo::~CMFCDesktopAlertWndInfo`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкдесктопалертвндинфо:: operator =](#operator_eq)||

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[Кмфкдесктопалертвндинфо:: m_hIcon](#m_hicon)|Маркер отображаемого значка.|
|[Кмфкдесктопалертвндинфо:: m_nURLCmdID](#m_nurlcmdid)|Идентификатор команды, связанный со ссылкой в окне оповещения рабочего стола.|
|[Кмфкдесктопалертвндинфо:: m_strText](#m_strtext)|Текст, отображаемый в окне оповещения рабочего стола.|
|[Кмфкдесктопалертвндинфо:: m_strURL](#m_strurl)|Ссылка, отображаемая в окне оповещения рабочего стола.|

## <a name="remarks"></a>Комментарии

`CMFCDesktopAlertWndInfo`Класс передается методу [CMFCDesktopAlertWnd:: Create](../../mfc/reference/cmfcdesktopalertwnd-class.md#create) для указания элементов, отображаемых в диалоговом окне оповещения рабочего стола по умолчанию. Диалоговое окно по умолчанию может содержать три элемента:

- Значок, который задается вызовом [кмфкдесктопалертвндинфо:: m_hIcon](#m_hicon).

- Метка или текстовое сообщение, которое задается вызовом [кмфкдесктопалертвндинфо:: m_strText](#m_strtext).

- Ссылка, которая задается вызовом [кмфкдесктопалертвндинфо:: m_strURL](#m_strurl). Чтобы задать команду, которая выполняется при нажатии ссылки, вызовите метод [кмфкдесктопалертвндинфо:: m_nURLCmdID](#m_nurlcmdid).

Если диалоговое окно по умолчанию не является достаточным, можно создать пользовательское диалоговое окно и передать его методу [CMFCDesktopAlertWnd:: Create](../../mfc/reference/cmfcdesktopalertwnd-class.md#create) , а не использовать этот класс. Дополнительные сведения см. в разделе [класс кмфкдесктопалертдиалог](../../mfc/reference/cmfcdesktopalertdialog-class.md).

## <a name="example"></a>Пример

В следующем примере показано, как использовать различные члены `CMFCDesktopAlertWndInfo` класса. В примере показано, как задать для маркера отображаемый значок, текст, отображаемый в окне оповещения рабочего стола, ссылка, отображаемая в окне оповещения рабочего стола, и идентификатор команды, связанный со ссылкой в окне оповещения рабочего стола. Этот пример является частью [демонстрационного примера оповещения Desktop](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_DesktopAlertDemo#3](../../mfc/reference/codesnippet/cpp/cmfcdesktopalertwndinfo-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CMFCDesktopAlertWndInfo](../../mfc/reference/cmfcdesktopalertwndinfo-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксдесктопалертдиалог. h

## <a name="cmfcdesktopalertwndinfooperator"></a><a name="operator_eq"></a> Кмфкдесктопалертвндинфо:: operator =

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
CMFCDesktopAlertWndInfo& operator=(CMFCDesktopAlertWndInfo& src);
```

### <a name="parameters"></a>Параметры

окне *src*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertwndinfom_hicon"></a><a name="m_hicon"></a> Кмфкдесктопалертвндинфо:: m_hIcon

Маркер отображаемого значка.

```
HICON m_hIcon;
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertwndinfom_nurlcmdid"></a><a name="m_nurlcmdid"></a> Кмфкдесктопалертвндинфо:: m_nURLCmdID

Идентификатор команды, связанный со ссылкой в окне оповещения рабочего стола.

```
UINT m_nURLCmdID;
```

### <a name="remarks"></a>Комментарии

Идентификатор команды отправляется владельцу всплывающего окна, когда пользователь щелкает ссылку, указанную параметром [кмфкдесктопалертвндинфо:: m_strURL](#m_strurl).

## <a name="cmfcdesktopalertwndinfom_strtext"></a><a name="m_strtext"></a> Кмфкдесктопалертвндинфо:: m_strText

Текст, отображаемый в окне оповещения рабочего стола.

```
CString m_strText;
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcdesktopalertwndinfom_strurl"></a><a name="m_strurl"></a> Кмфкдесктопалертвндинфо:: m_strURL

Ссылка, отображаемая в окне оповещения рабочего стола.

```
CString m_strURL;
```

### <a name="remarks"></a>Комментарии

Когда пользователь щелкнет ссылку, команда с ИДЕНТИФИКАТОРом команды [кмфкдесктопалертвндинфо:: m_nURLCmdID](#m_nurlcmdid) будет отправлена владельцу всплывающего окна.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCDesktopAlertWnd](../../mfc/reference/cmfcdesktopalertwnd-class.md)<br/>
[CMFCDesktopAlertWnd:: Create](../../mfc/reference/cmfcdesktopalertwnd-class.md#create)<br/>
[Класс Кмфкдесктопалертдиалог](../../mfc/reference/cmfcdesktopalertdialog-class.md)
