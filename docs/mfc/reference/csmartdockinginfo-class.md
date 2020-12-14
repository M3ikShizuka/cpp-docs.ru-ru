---
description: 'Дополнительные сведения о: Ксмартдоккингинфо Class'
title: Класс Ксмартдоккингинфо
ms.date: 11/19/2018
f1_keywords:
- CSmartDockingInfo
- AFXDOCKINGMANAGER/CSmartDockingInfo
- AFXDOCKINGMANAGER/CSmartDockingInfo::CopyTo
- AFXDOCKINGMANAGER/CSmartDockingInfo::m_bUseThemeColorInShading
- AFXDOCKINGMANAGER/CSmartDockingInfo::m_clrBaseBackground
- AFXDOCKINGMANAGER/CSmartDockingInfo::m_clrToneDest
- AFXDOCKINGMANAGER/CSmartDockingInfo::m_clrToneSrc
- AFXDOCKINGMANAGER/CSmartDockingInfo::m_clrTransparent
- AFXDOCKINGMANAGER/CSmartDockingInfo::m_nCentralGroupOffset
- AFXDOCKINGMANAGER/CSmartDockingInfo::m_sizeTotal
- AFXDOCKINGMANAGER/CSmartDockingInfo::m_uiMarkerBmpResID
- AFXDOCKINGMANAGER/CSmartDockingInfo::m_uiMarkerLightBmpResID
helpviewer_keywords:
- CSmartDockingInfo [MFC], CopyTo
- CSmartDockingInfo [MFC], m_bUseThemeColorInShading
- CSmartDockingInfo [MFC], m_clrBaseBackground
- CSmartDockingInfo [MFC], m_clrToneDest
- CSmartDockingInfo [MFC], m_clrToneSrc
- CSmartDockingInfo [MFC], m_clrTransparent
- CSmartDockingInfo [MFC], m_nCentralGroupOffset
- CSmartDockingInfo [MFC], m_sizeTotal
- CSmartDockingInfo [MFC], m_uiMarkerBmpResID
- CSmartDockingInfo [MFC], m_uiMarkerLightBmpResID
ms.assetid: cab04f38-4bc1-4378-9337-c56fc87fbd68
ms.openlocfilehash: 290f9eef208ceed425739ab26e7811c04309e057
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97345138"
---
# <a name="csmartdockinginfo-class"></a>Класс Ксмартдоккингинфо

Определяет внешний вид интеллектуальных маркеров закрепления.

## <a name="syntax"></a>Синтаксис

```
class CSmartDockingInfo : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CSmartDockingInfo::CSmartDockingInfo`|Конструктор по умолчанию.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксмартдоккингинфо:: CopyTo](#copyto)|Копирует текущие параметры сведений о смарт-закреплениях в указанный объект [ксмартдоккингинфо](../../mfc/reference/csmartdockinginfo-class.md) .|

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[Ксмартдоккингинфо:: m_bUseThemeColorInShading](#m_busethemecolorinshading)|Указывает, следует ли использовать текущий цвет темы, когда платформа отображает маркеры смарт-закрепления.|
|[Ксмартдоккингинфо:: m_clrBaseBackground](#m_clrbasebackground)|Задает основной цвет фона для маркеров смарт-закрепления.|
|[Ксмартдоккингинфо:: m_clrToneDest](#m_clrtonedest)|Задает цвет, который заменяется `m_clrToneSrc` в точечных рисунках маркера смарт-стыковки.|
|[Ксмартдоккингинфо:: m_clrToneSrc](#m_clrtonesrc)|Задает цвет битовых карт для маркера смарт-закрепления.|
|[Ксмартдоккингинфо:: m_clrTransparent](#m_clrtransparent)|Задает цвет битовых карт для маркера смарт-закрепления, если они являются прозрачными.|
|[Ксмартдоккингинфо:: m_nCentralGroupOffset](#m_ncentralgroupoffset)|Задает смещение центральной группы маркеров геостыковки от границ прямоугольника центральной группы.|
|[Ксмартдоккингинфо:: m_sizeTotal](#m_sizetotal)|Задает общий размер всех маркеров смарт-закрепления в группе.|
|[Ксмартдоккингинфо:: m_uiMarkerBmpResID](#m_uimarkerbmpresid)|Определяет идентификаторы ресурсов точечных рисунков, используемых платформой для невыделенных маркеров смарт-закрепления.|
|[Ксмартдоккингинфо:: m_uiMarkerLightBmpResID](#m_uimarkerlightbmpresid)|Определяет идентификаторы ресурсов точечных рисунков, используемых платформой для выделенных маркеров смарт-закрепления.|

## <a name="remarks"></a>Комментарии

Платформа обрабатывает маркеры смарт-закрепления внутренним образом. На следующем рисунке показаны стандартные маркеры смарт-закрепления:

![Стандартные маркеры смарт-закрепления](../../mfc/reference/media/nextsdmarkers.png "Стандартные маркеры смарт-закрепления")

На этом рисунке в изображении слева показан Центрально закрепленный маркер группы, который не поддерживает прикрепление к вкладке. Изображение в середине показывает правый маркер смарт-закрепления. На изображении справа отображается Центральный маркер геостыковки группы, в котором включена закрепление на вкладке. В центральном маркере смарт-стыковки есть основной точечный рисунок и пять битовых карт для маркера закрепления.

Можно настроить следующие параметры для маркеров смарт-закрепления:

- Цвет. Например, можно заменить синий цвет маркеров на рисунке на любой определенный пользователем цвет.

- Цвет прозрачности.

- Смещение маркера смарт-закрепления в Центральной группе от границы ограничивающего прямоугольника.

- Основной точечный рисунок, представляющий центральную группу.

- Точечные рисунки, представляющие регулярные и выделенные маркеры смарт-закрепления.

На следующем рисунке показан пример настраиваемых маркеров закрепления:

![Пользовательские маркеры смарт-закрепления](../../mfc/reference/media/nextsdmarkerscustom.png "Пользовательские маркеры смарт-закрепления")

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CSmartDockingInfo](../../mfc/reference/csmartdockinginfo-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксдоккингманажер. h

## <a name="csmartdockinginfocopyto"></a><a name="copyto"></a> Ксмартдоккингинфо:: CopyTo

Копирует текущие параметры смарт-стыковки в указанный объект [ксмартдоккингинфо](../../mfc/reference/csmartdockinginfo-class.md) .

```cpp
void CopyTo(CSmartDockingInfo& params);
```

### <a name="parameters"></a>Параметры

*params*<br/>
заполняет Объект типа `CSmartDockingInfo` , заполненный текущими параметрами смарт-стыковки.

## <a name="csmartdockinginfom_busethemecolorinshading"></a><a name="m_busethemecolorinshading"></a> Ксмартдоккингинфо:: m_bUseThemeColorInShading

Указывает, следует ли использовать текущий цвет темы, когда платформа отображает маркеры смарт-закрепления.

```
BOOL m_bUseThemeColorInShading;
```

### <a name="remarks"></a>Комментарии

Если значение равно TRUE, маркеры рисуются с использованием текущего цвета темы; в противном случае маркеры рисуются с помощью светло-синего цвета.

Значение по умолчанию — FALSE.

## <a name="csmartdockinginfom_clrbasebackground"></a><a name="m_clrbasebackground"></a> Ксмартдоккингинфо:: m_clrBaseBackground

Задает основной цвет фона для маркеров смарт-закрепления.

```
COLORREF m_clrBaseBackground;
```

## <a name="csmartdockinginfom_clrtonedest"></a><a name="m_clrtonedest"></a> Ксмартдоккингинфо:: m_clrToneDest

Задает цвет, который будет заменен `m_clrToneSrc` в точечных рисунках маркера смарт-стыковки.

```
COLORREF m_clrToneDest;
```

### <a name="remarks"></a>Комментарии

Задайте это значение, чтобы программно изменить цвет битовой карты маркера. Например, если вы хотите изменить цвет стандартных маркеров, предоставляемых платформой, задайте для этого параметра требуемый цвет. По умолчанию [ксмартдоккингинфо:: m_clrToneSrc](#m_clrtonesrc) имеет значение RGB (61, 123, 241) (блуиш Color).

Чтобы изменить цвет пользовательских маркеров, необходимо указать `m_clrToneDest` и `m_clrToneSrc` .

## <a name="csmartdockinginfom_clrtonesrc"></a><a name="m_clrtonesrc"></a> Ксмартдоккингинфо:: m_clrToneSrc

Задает цвет битовых карт для маркера смарт-закрепления.

```
COLORREF m_clrToneSrc;
```

### <a name="remarks"></a>Комментарии

Это значение задается только в том случае, если требуется заменить цвет пользовательского точечного рисунка другим цветом. Это значение задавать не нужно, если изменяется цвет маркера стандартного (предоставленная платформой).

Используйте `(COLORREF)-1` , чтобы оставить член группы смарт-закрепления пустым.

## <a name="csmartdockinginfom_clrtransparent"></a><a name="m_clrtransparent"></a> Ксмартдоккингинфо:: m_clrTransparent

Задает цвет битовых карт для маркера смарт-закрепления, если они являются прозрачными.

```
COLORREF m_clrTransparent;
```

### <a name="remarks"></a>Комментарии

Это значение необходимо задать при отображении пользовательских маркеров и пользовательских точечных рисунков в группе закрепления.

## <a name="csmartdockinginfom_ncentralgroupoffset"></a><a name="m_ncentralgroupoffset"></a> Ксмартдоккингинфо:: m_nCentralGroupOffset

Задает смещение между Центральной группой маркеров смарт-закрепления и границами прямоугольника центральной группы.

```
int m_nCentralGroupOffset;
```

### <a name="remarks"></a>Комментарии

Укажите это значение, если необходимо изменить смещение по умолчанию между пользовательскими маркерами и границами Центральной группы в маркерах смарт-закрепления. Смещение по умолчанию — 5 пикселей.

## <a name="csmartdockinginfom_sizetotal"></a><a name="m_sizetotal"></a> Ксмартдоккингинфо:: m_sizeTotal

Задает общий размер ограничивающего прямоугольника, охватывающего все интеллектуальные маркеры закрепления в Центральной группе.

```
CSize m_sizeTotal;
```

### <a name="remarks"></a>Комментарии

Задайте `m_sizeTotal` размер ограничивающего прямоугольника маркера Центральной группы. Это значение необходимо указать, если для маркеров используются пользовательские точечные рисунки.

## <a name="csmartdockinginfom_uimarkerbmpresid"></a><a name="m_uimarkerbmpresid"></a> Ксмартдоккингинфо:: m_uiMarkerBmpResID

Определяет идентификаторы ресурсов точечных рисунков, используемых для невыделенных настраиваемых маркеров закрепления.

```
UINT m_uiMarkerBmpResID[AFX_SD_MARKERS_NUM];
```

### <a name="remarks"></a>Комментарии

Заполните этот массив идентификаторами ресурсов точечных рисунков, представляющих маркеры смарт-закрепления. AFX_SD_MARKERS_NUM в данный момент определен как 5. Массив заполняется следующим образом:

```cpp
params.m_uiMarkerBmpResID[0] = IDB_MARKER_LEFT;
params.m_uiMarkerBmpResID[1] = IDB_MARKER_RIGHT;
params.m_uiMarkerBmpResID[2] = IDB_MARKER_TOP;
params.m_uiMarkerBmpResID[3] = IDB_MARKER_BOTTOM;
params.m_uiMarkerBmpResID[4] = IDB_MARKER_CENTER;
```

## <a name="csmartdockinginfom_uimarkerlightbmpresid"></a><a name="m_uimarkerlightbmpresid"></a> Ксмартдоккингинфо:: m_uiMarkerLightBmpResID

Определяет идентификаторы ресурсов точечных рисунков, используемых для выделенных настраиваемых маркеров закрепления.

```
UINT m_uiMarkerLightBmpResID[AFX_SD_MARKERS_NUM];
```

### <a name="remarks"></a>Комментарии

Заполните этот массив идентификаторами ресурсов точечных рисунков, представляющих выделенные интеллектуальные маркеры закрепления. AFX_SD_MARKERS_NUM в данный момент определен как 5. Массив заполняется следующим образом:

```cpp
params.m_uiMarkerLightBmpResID[0] = IDB_MARKER_LEFT_LIGHT;
params.m_uiMarkerLightBmpResID[1] = IDB_MARKER_RIGHT_LIGHT;
params.m_uiMarkerLightBmpResID[2] = IDB_MARKER_TOP_LIGHT;
params.m_uiMarkerLightBmpResID[3] = IDB_MARKER_BOTTOM_LIGHT;
params.m_uiMarkerLightBmpResID[4] = IDB_MARKER_CENTER_LIGHT;
```

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[CObject, класс](../../mfc/reference/cobject-class.md)
