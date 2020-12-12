---
description: 'Дополнительные сведения о: перечисление CMFCImagePaintArea:: IMAGE_EDIT_MODE enumeration'
title: Перечисление CMFCImagePaintArea::IMAGE_EDIT_MODE
ms.date: 11/04/2016
f1_keywords:
- IMAGE_EDIT_MODE Enumeration
helpviewer_keywords:
- IMAGE_EDIT_MODE Enumeration method [MFC]
ms.assetid: e51db66a-fa1c-4766-9dac-a25b595f871a
ms.openlocfilehash: f28880d108be8fb4f2b14ede1a3cbd3c7dac9f2e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97265328"
---
# <a name="cmfcimagepaintareaimage_edit_mode-enumeration"></a>Перечисление CMFCImagePaintArea::IMAGE_EDIT_MODE

Задает режим рисования, используемый для изменения изображения в диалоговом окне редактора изображений.

## <a name="syntax"></a>Синтаксис

```
enum IMAGE_EDIT_MODE
{
    IMAGE_EDIT_MODE_PEN = 0,
    IMAGE_EDIT_MODE_FILL,
    IMAGE_EDIT_MODE_LINE,
    IMAGE_EDIT_MODE_RECT,
    IMAGE_EDIT_MODE_ELLIPSE,
    IMAGE_EDIT_MODE_COLOR
};
```

## <a name="members"></a>Члены

|Имя|Описание|
|-|-|
|IMAGE_EDIT_MODE_PEN|Используется для рисования отдельных пикселов.|
|IMAGE_EDIT_MODE_FILL|Используется для заполнения всех смежных областей, содержащих цвет в текущем положении курсора.|
|IMAGE_EDIT_MODE_LINE|Используется для рисования линии.|
|IMAGE_EDIT_MODE_RECT|Используется для рисования прямоугольника.|
|IMAGE_EDIT_MODE_ELLIPSE|Используется для рисования эллипса.|
|IMAGE_EDIT_MODE_COLOR|Используется для установки текущего цвета на цвет в текущем положении курсора.|

### <a name="remarks"></a>Комментарии

`CMFCImagePaintArea`Классы и `CMFCImageEditorDialog` используют это перечисление для установки текущего режима рисования. Режим рисования и текущий цвет используются для изменения области изображения в диалоговом окне редактора изображений. Дополнительные сведения о `CMFCImagePaintArea` и `CMFCImageEditorDialog` см. в разделе [класс перечисление CMFCImagePaintArea](../../mfc/reference/cmfcimagepaintarea-class.md) и [класс кмфЦимажеедитордиалог](../../mfc/reference/cmfcimageeditordialog-class.md).

При выборе цвета из изображения с помощью IMAGE_EDIT_MODE_COLOR режима рисования платформа устанавливает для текущего режима рисования значение IMAGE_EDIT_MODE_PEN.

## <a name="requirements"></a>Требования

**Заголовок:** афксимажепаинтареа. h

## <a name="see-also"></a>См. также раздел

[Макросы и глобальные объекты](../../mfc/reference/mfc-macros-and-globals.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс перечисление CMFCImagePaintArea](../../mfc/reference/cmfcimagepaintarea-class.md)<br/>
[Класс КмфЦимажеедитордиалог](../../mfc/reference/cmfcimageeditordialog-class.md)
