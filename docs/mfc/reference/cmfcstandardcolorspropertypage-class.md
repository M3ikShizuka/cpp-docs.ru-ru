---
description: 'Дополнительные сведения о: Кмфкстандардколорспропертипаже Class'
title: Класс Кмфкстандардколорспропертипаже
ms.date: 11/04/2016
helpviewer_keywords:
- CMFCStandardColorsPropertyPage class [MFC]
ms.assetid: b84b7cfb-bb24-4c65-804a-5b642cb64400
ms.openlocfilehash: cffce34642bd4df40ceda3156fe846e60db4b3a6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97164098"
---
# <a name="cmfcstandardcolorspropertypage-class"></a>Класс Кмфкстандардколорспропертипаже

Представляет страницу свойств, используемую пользователями для выбора стандартных цветов в диалоговом окне цвета.

## <a name="syntax"></a>Синтаксис

```
class CMFCStandardColorsPropertyPage : public CPropertyPage
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|-|-|
|`CMFCStandardColorsPropertyPage::CMFCStandardColorsPropertyPage`|Конструктор по умолчанию.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|-|-|
|`CMFCStandardColorsPropertyPage::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|`CMFCStandardColorsPropertyPage::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|

### <a name="remarks"></a>Комментарии

`CMFCColorDialog`Класс использует этот класс для вывода страницы свойств стандартного цвета. Дополнительные сведения о см `CMFCColorDialog` . в разделе [класс кмфкколордиалог](../../mfc/reference/cmfccolordialog-class.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CPropertyPage](../../mfc/reference/cpropertypage-class.md)

[кмфкстандардколорспропертипаже](../../mfc/reference/cmfcstandardcolorspropertypage-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксстандардколорспропертипаже. h

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкколордиалог](../../mfc/reference/cmfccolordialog-class.md)<br/>
[Класс Кмфккустомколорспропертипаже](../../mfc/reference/cmfccustomcolorspropertypage-class.md)
