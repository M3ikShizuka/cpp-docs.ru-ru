---
description: 'Дополнительные сведения о: КмфЦимажеедитордиалог Class'
title: Класс КмфЦимажеедитордиалог
ms.date: 11/19/2018
f1_keywords:
- CMFCImageEditorDialog
- AFXIMAGEEDITORDIALOG/CMFCImageEditorDialog
- AFXIMAGEEDITORDIALOG/CMFCImageEditorDialog::CMFCImageEditorDialog
helpviewer_keywords:
- CMFCImageEditorDialog [MFC], CMFCImageEditorDialog
ms.assetid: 6a7d08f3-1ec2-4062-9b79-a0c2776b58d1
ms.openlocfilehash: 6c25cf4a1a8d0cc5852049a06c3a140cbb00a118
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97265393"
---
# <a name="cmfcimageeditordialog-class"></a>Класс КмфЦимажеедитордиалог

`CMFCImageEditorDialog`Класс поддерживает диалоговое окно Редактор изображений.

## <a name="syntax"></a>Синтаксис

```
class CMFCImageEditorDialog : public CDialogEx
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[КмфЦимажеедитордиалог:: КмфЦимажеедитордиалог](#cmfcimageeditordialog)|Формирует объект `CMFCImageEditorDialog`.|

## <a name="remarks"></a>Комментарии

`CMFCImageEditorDialog`Класс предоставляет диалоговое окно, которое включает:

- Область изображения, используемая для изменения отдельных пикселов в изображении.

- Средства рисования для изменения пикселов в области изображения.

- Цветовая палитра для указания цвета, используемого инструментами рисования.

- Область предварительного просмотра, в которой отображается результат изменения.

На следующем рисунке показано диалоговое окно Редактор изображений.

![Диалоговое окно CMFCImageEditorDialog](../../mfc/reference/media/imageedit.png "Диалоговое окно CMFCImageEditorDialog")

Один из способов использования `CMFCImageEditorDialog` объекта — передать ему `CBitmap` изображение для редактирования. Не создавайте крупные изображения, так как область редактирования изображений имеет ограниченный размер, а размер логического пикселя изменяется в соответствии с областью. Вызовите `DoModal` метод, чтобы запустить модальное диалоговое окно.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CDialogEx](../../mfc/reference/cdialogex-class.md)

[CMFCImageEditorDialog](../../mfc/reference/cmfcimageeditordialog-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксимажеедитордиалог. h

## <a name="cmfcimageeditordialogcmfcimageeditordialog"></a><a name="cmfcimageeditordialog"></a> КмфЦимажеедитордиалог:: КмфЦимажеедитордиалог

Формирует объект `CMFCImageEditorDialog`.

```
CMFCImageEditorDialog(
    CBitmap* pBitmap,
    CWnd* pParent=NULL,
    int nBitsPixel=-1);
```

### <a name="parameters"></a>Параметры

*пбитмап*<br/>
Указатель на изображение.

*ппарент*<br/>
Указатель на родительское окно диалогового окна редактора текущего изображения.

*нбитспиксел*<br/>
Число битов, используемых для представления цвета одного пикселя, который также называется глубиной цвета.  Если параметр *нбитспиксел* имеет значение-1, глубина цвета определяется на основе изображения, указанного параметром *пбитмап* . Значение по умолчанию — -1.

### <a name="return-value"></a>Возвращаемое значение

Чтобы изменить изображение, передайте указатель на изображение в `CMFCImageEditorDialog` конструктор. Затем вызовите `DoModal` метод, чтобы открыть модальное диалоговое окно. Когда `DoModal` метод возвращает значение, точечный рисунок содержит новый образ.

### <a name="remarks"></a>Remarks

### <a name="example"></a>Пример

В следующем примере показано, как создать объект `CMFCImageEditorDialog` класса. Этот пример является частью [примера новых элементов управления](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_NewControls#8](../../mfc/reference/codesnippet/cpp/cmfcimageeditordialog-class_1.cpp)]
[!code-cpp[NVC_MFC_NewControls#40](../../mfc/reference/codesnippet/cpp/cmfcimageeditordialog-class_2.cpp)]

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)
