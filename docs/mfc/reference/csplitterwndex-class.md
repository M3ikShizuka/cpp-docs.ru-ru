---
description: 'Дополнительные сведения о: Ксплиттервндекс Class'
title: Класс Ксплиттервндекс
ms.date: 11/04/2016
f1_keywords:
- CSplitterWndEx
- AFXSPLITTERWNDEX/CSplitterWndEx
- AFXSPLITTERWNDEX/CSplitterWndEx::OnDrawSplitter
helpviewer_keywords:
- CSplitterWndEx [MFC], OnDrawSplitter
ms.assetid: 33e5eef3-05e1-4a07-a968-bf9207ce8598
ms.openlocfilehash: 357f650551871cc9768c8e4e693bd62bb5e69bc4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97345099"
---
# <a name="csplitterwndex-class"></a>Класс Ксплиттервндекс

Представляет настроенное окно-разделитель.

## <a name="syntax"></a>Синтаксис

```
class CSplitterWndEx : public CSplitterWnd
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CSplitterWndEx::CSplitterWndEx`|Конструктор по умолчанию.|
|`CSplitterWndEx::~CSplitterWndEx`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксплиттервндекс:: Ондравсплиттер](#ondrawsplitter)|Вызывается платформой для рисования окна-разделителя. (Переопределяет [CSplitterWnd:: ондравсплиттер](csplitterwnd-class.md#ondrawsplitter).)|

## <a name="remarks"></a>Комментарии

Переопределите `OnDrawSplitter` метод, чтобы настроить внешний вид графических компонентов окна-разделителя.

`CSplitterWndEx`Класс используется вместе с методами [ондравсплиттербордер](cmfcvisualmanager-class.md#ondrawsplitterborder), [ондравсплиттербокс](cmfcvisualmanager-class.md#ondrawsplitterbox)и [онфиллсплиттербаккграунд](cmfcvisualmanager-class.md#onfillsplitterbackground) , которые реализуются визуальным диспетчером. Чтобы визуальный диспетчер выводил в приложении разделительное окно, замените объявления `CSplitterWnd` класса `CSplitterWndEx` классом. Для приложений фреймовых окон класс Window-разделителя объявляется в классе CMainFrame, который находится в маинфрм. h. Пример см. в примере `OutlookDemo` в каталоге Samples.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](cobject-class.md)

[CCmdTarget](ccmdtarget-class.md)

[CWnd](cwnd-class.md)

[CSplitterWnd](csplitterwnd-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкссплиттервндекс. h

## <a name="csplitterwndexondrawsplitter"></a><a name="ondrawsplitter"></a> Ксплиттервндекс:: Ондравсплиттер

Вызывается платформой для рисования окна-разделителя.

```
virtual void OnDrawSplitter(
   CDC* pDC,
   ESplitType nType,
   const CRect& rect
);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства. Если этот параметр имеет значение NULL, платформа перерисовывает активное окно.

*nType*<br/>
окне Одно из `CSplitterWnd::ESplitType` значений перечисления, указывающее рисуемый элемент разделителя окна. Допустимые значения: `splitBox`, `splitBar`, `splitIntersection` и `splitBorder`.

*rect*<br/>
окне Ограничивающий прямоугольник, указывающий размеры и расположение для рисования заданного элемента разделителя.

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../hierarchy-chart.md)<br/>
[Классы](mfc-classes.md)<br/>
[Класс CSplitterWnd](csplitterwnd-class.md)<br/>
[Класс CMFCVisualManager](cmfcvisualmanager-class.md)
