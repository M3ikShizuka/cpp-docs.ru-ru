---
description: 'Дополнительные сведения о: Кмфккустомколорспропертипаже Class'
title: Класс Кмфккустомколорспропертипаже
ms.date: 11/04/2016
f1_keywords:
- CMFCCustomColorsPropertyPage
- AFXCUSTOMCOLORSPROPERTYPAGE/CMFCCustomColorsPropertyPage
- AFXCUSTOMCOLORSPROPERTYPAGE/CMFCCustomColorsPropertyPage::Setup
helpviewer_keywords:
- CMFCCustomColorsPropertyPage [MFC], Setup
ms.assetid: 46a45ba2-1fda-440d-8018-d4dcd44f5816
ms.openlocfilehash: 9a1e5a83f2dcb291b266c3ef8fcd65422d30135a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193348"
---
# <a name="cmfccustomcolorspropertypage-class"></a>Класс Кмфккустомколорспропертипаже

Представляет страницу свойств, которая может выбирать пользовательские цвета в диалоговом окне цвета.

## <a name="syntax"></a>Синтаксис

```
class CMFCCustomColorsPropertyPage : public CPropertyPage
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|-|-|
|`CMFCCustomColorsPropertyPage::CMFCCustomColorsPropertyPage`|Конструктор по умолчанию.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|-|-|
|`CMFCCustomColorsPropertyPage::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|`CMFCCustomColorsPropertyPage::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|
|[Кмфккустомколорспропертипаже:: Setup](#setup)|Задает компоненты цвета страницы свойств.|

### <a name="remarks"></a>Комментарии

`CMFCColorDialog`Класс использует этот класс для вывода страницы свойств пользовательского цвета. Дополнительные сведения о см `CMFCColorDialog` . в разделе [класс кмфкколордиалог](../../mfc/reference/cmfccolordialog-class.md).

## <a name="example"></a>Пример

В следующем примере показано, как создать `CMFCCustomColorsPropertyPage` объект и установить цветовые компоненты страницы свойств.

[!code-cpp[NVC_MFC_RibbonApp#35](../../mfc/reference/codesnippet/cpp/cmfccustomcolorspropertypage-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CPropertyPage](../../mfc/reference/cpropertypage-class.md)

[кмфккустомколорспропертипаже](../../mfc/reference/cmfccustomcolorspropertypage-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкскустомколорспропертипаже. h

## <a name="cmfccustomcolorspropertypagesetup"></a><a name="setup"></a> Кмфккустомколорспропертипаже:: Setup

Задает компоненты цвета страницы свойств.

```cpp
void Setup(
    BYTE R,
    BYTE G,
    BYTE B);
```

### <a name="parameters"></a>Параметры

*Cерверный*\
окне Красный компонент значения RGB.

*Модуле*\
окне Зеленый компонент значения RGB.

*&*\
окне Синий компонент значения RGB.

### <a name="remarks"></a>Комментарии

Этот метод обновляет текущие значения цвета RGB и связанные HLS (оттенок, освещение и насыщенность) на странице свойств. Метод [кмфкколордиалог:: сетпажетво](../../mfc/reference/cmfccolordialog-class.md#setpagetwo) вызывает этот метод, когда платформа Инициализирует диалоговое окно цвета или пользователь нажимает левую кнопку мыши. Дополнительные сведения о см `CMFCColorDialog` . в разделе [класс кмфкколордиалог](../../mfc/reference/cmfccolordialog-class.md).

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкколордиалог](../../mfc/reference/cmfccolordialog-class.md)<br/>
[Класс Кмфкстандардколорспропертипаже](../../mfc/reference/cmfcstandardcolorspropertypage-class.md)
