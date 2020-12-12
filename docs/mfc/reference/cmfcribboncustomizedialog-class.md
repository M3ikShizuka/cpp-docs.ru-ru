---
description: 'Дополнительные сведения о: Кмфкриббонкустомизедиалог Class'
title: Класс Кмфкриббонкустомизедиалог
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonCustomizeDialog
- AFXRIBBONCUSTOMIZEDIALOG/CMFCRibbonCustomizeDialog
- AFXRIBBONCUSTOMIZEDIALOG/CMFCRibbonCustomizeDialog::CMFCRibbonCustomizeDialog
helpviewer_keywords:
- CMFCRibbonCustomizeDialog [MFC], CMFCRibbonCustomizeDialog
ms.assetid: ce67de7f-5eaa-4c75-9b94-f290f36df073
ms.openlocfilehash: 9420ebdf32a1c26cba6efee17467fd3dfe202574
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97293616"
---
# <a name="cmfcribboncustomizedialog-class"></a>Класс Кмфкриббонкустомизедиалог

Отображает страницу **настройки** ленты.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonCustomizeDialog : public CMFCPropertySheet
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонкустомизедиалог:: Кмфкриббонкустомизедиалог](#cmfcribboncustomizedialog)|Формирует объект `CMFCRibbonCustomizeDialog`.|
|`CMFCRibbonCustomizeDialog::~CMFCRibbonCustomizeDialog`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|`CMFCRibbonCustomizeDialog::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|

## <a name="remarks"></a>Комментарии

MFC создает этот класс автоматически, если вы не обрабатываете AFX_WM_ON_RIBBON_CUSTOMIZE сообщение или возвращает 0 из обработчика сообщений.

Если вы хотите использовать этот класс в приложении для вывода диалогового окна **Настройка** ленты, просто создайте его экземпляр и вызовите `DoModal` метод.

Поскольку этот класс является производным от [класса кмфкпропертишит](../../mfc/reference/cmfcpropertysheet-class.md), можно добавить пользовательские страницы с помощью `CMFCPropertySheet` API.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CPropertySheet](../../mfc/reference/cpropertysheet-class.md)

[CMFCPropertySheet](../../mfc/reference/cmfcpropertysheet-class.md)

[кмфкриббонкустомизедиалог](../../mfc/reference/cmfcribboncustomizedialog-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонкустомизедиалог. h

## <a name="cmfcribboncustomizedialogcmfcribboncustomizedialog"></a><a name="cmfcribboncustomizedialog"></a> Кмфкриббонкустомизедиалог:: Кмфкриббонкустомизедиалог

Формирует объект `CMFCRibbonCustomizeDialog`.

```
CMFCRibbonCustomizeDialog(
    CWnd* pWndParent,
    CMFCRibbonBar* pRibbon);
```

### <a name="parameters"></a>Параметры

*пвндпарент*<br/>
окне Указатель на родительское окно (обычно это основной фрейм).

*приббон*<br/>
окне Указатель на объект `CMFCRibbonBar` , который необходимо настроить.

### <a name="example"></a>Пример

В следующем примере показано, как создать `CMFCRibbonCustomizeDialog` объект.

[!code-cpp[NVC_MFC_RibbonApp#18](../../mfc/reference/codesnippet/cpp/cmfcribboncustomizedialog-class_1.cpp)]

### <a name="remarks"></a>Комментарии

Конструктор создает экземпляр объекта [класса кмфкриббонкустомизепропертипаже](../../mfc/reference/cmfcribboncustomizepropertypage-class.md) и добавляет его в коллекцию страниц страницы свойств.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)
