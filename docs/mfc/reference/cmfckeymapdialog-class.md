---
description: 'Дополнительные сведения о: Кмфккэймапдиалог Class'
title: Класс Кмфккэймапдиалог
ms.date: 11/04/2016
f1_keywords:
- CMFCKeyMapDialog
- AFXKEYMAPDIALOG/CMFCKeyMapDialog
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::CMFCKeyMapDialog
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::DoModal
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::FormatItem
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::GetCommandKeys
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::OnInsertItem
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::OnPrintHeader
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::OnPrintItem
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::OnSetColumns
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::PrintKeyMap
- AFXKEYMAPDIALOG/CMFCKeyMapDialog::SetColumnsWidth
helpviewer_keywords:
- CMFCKeyMapDialog [MFC], CMFCKeyMapDialog
- CMFCKeyMapDialog [MFC], DoModal
- CMFCKeyMapDialog [MFC], FormatItem
- CMFCKeyMapDialog [MFC], GetCommandKeys
- CMFCKeyMapDialog [MFC], OnInsertItem
- CMFCKeyMapDialog [MFC], OnPrintHeader
- CMFCKeyMapDialog [MFC], OnPrintItem
- CMFCKeyMapDialog [MFC], OnSetColumns
- CMFCKeyMapDialog [MFC], PrintKeyMap
- CMFCKeyMapDialog [MFC], SetColumnsWidth
ms.assetid: 5feb4942-d636-462d-a162-0104dd320f4e
ms.openlocfilehash: e339edb54b9c381dd2b27c9ee3ec7566308ae434
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97265237"
---
# <a name="cmfckeymapdialog-class"></a>Класс Кмфккэймапдиалог

`CMFCKeyMapDialog`Класс поддерживает элемент управления, который сопоставляет команды с клавишами на клавиатуре.

## <a name="syntax"></a>Синтаксис

```
class CMFCKeyMapDialog : public CDialogEx
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфккэймапдиалог:: Кмфккэймапдиалог](#cmfckeymapdialog)|Формирует объект `CMFCKeyMapDialog`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфккэймапдиалог::D Омодал](#domodal)|Отображает диалоговое окно расстановка клавиатуры.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кмфккэймапдиалог:: Форматитем](#formatitem)|Вызывается платформой для создания строки, описывающей сопоставление ключей. По умолчанию строка содержит имя команды, используемые сочетания клавиш и описание сочетания клавиш.|
|[Кмфккэймапдиалог:: Жеткоммандкэйс](#getcommandkeys)|Извлекает строку, содержащую список сочетаний клавиш, связанных с указанной командой.|
|[Кмфккэймапдиалог:: Онинсертитем](#oninsertitem)|Вызвано структурой перед вставкой нового элемента в внутренний элемент управления "список", поддерживающий элемент управления "сопоставление клавиш".|
|[Кмфккэймапдиалог:: Онпринсеадер](#onprintheader)|Вызывается платформой для печати заголовка для схемы клавиатуры на новой странице.|
|[Кмфккэймапдиалог:: Онпринтитем](#onprintitem)|Вызывается платформой для печати элемента назначения клавиатуры.|
|[Кмфккэймапдиалог:: Онсетколумнс](#onsetcolumns)|Вызывается платформой для установки заголовков столбцов во внутреннем элементе управления "список", поддерживающем элемент управления "сопоставление клавиш".|
|[Кмфккэймапдиалог::P Ринткэймап](#printkeymap)|Вызывается платформой при нажатии пользователем кнопки " **Печать** ".|
|[Кмфккэймапдиалог:: Сетколумнсвидс](#setcolumnswidth)|Вызывается платформой для установки ширины столбцов в элементе управления "внутренний список", поддерживающем элемент управления "сопоставление клавиш".|

## <a name="remarks"></a>Комментарии

Используйте `CMFCKeyMapDialog` класс для реализации диалогового окна сопоставления клавиш с изменяемым размером. Диалоговое окно использует элемент управления "представление списка" для отображения сочетаний клавиш и связанных с ними команд.

Чтобы использовать `CMFCKeyMapDialog` класс в приложении, передайте указатель на главное окно фрейма в качестве параметра в `CMFCKeyMapDialog` конструктор. Затем вызовите `DoModal` метод, чтобы запустить модальное диалоговое окно.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CDialogEx](../../mfc/reference/cdialogex-class.md)

[CMFCKeyMapDialog](../../mfc/reference/cmfckeymapdialog-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкскэймапдиалог. h

## <a name="cmfckeymapdialogcmfckeymapdialog"></a><a name="cmfckeymapdialog"></a> Кмфккэймапдиалог:: Кмфккэймапдиалог

Формирует объект `CMFCKeyMapDialog`.

```
CMFCKeyMapDialog(
    CFrameWnd* pWndParentFrame,
    BOOL bEnablePrint=FALSE);
```

### <a name="parameters"></a>Параметры

*пвндпарентфраме*<br/>
окне Указатель на родительское окно `CMFCKeyMapDialog` объекта.

*бенаблепринт*<br/>
окне Значение TRUE, если список сочетаний клавиш можно распечатать; в противном случае — значение FALSE. Значение по умолчанию — FALSE.

### <a name="remarks"></a>Remarks

### <a name="example"></a>Пример

В следующем примере показано, как создать объект `CMFCKeyMapDialog` класса. Этот пример является частью [демонстрационного примера Visual Studio](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_VisualStudioDemo#21](../../mfc/codesnippet/cpp/cmfckeymapdialog-class_1.cpp)]

## <a name="cmfckeymapdialogdomodal"></a><a name="domodal"></a> Кмфккэймапдиалог::D Омодал

Отображает диалоговое окно расстановка клавиатуры.

```
virtual INT_PTR DoModal();
```

### <a name="return-value"></a>Возвращаемое значение

Целое число со знаком, например ИДОК или ИДКАНЦЕЛ, которое передается методу [CDialog:: EndDialog](../../mfc/reference/cdialog-class.md#enddialog) . Метод, в свою очередь, закрывает диалоговое окно. Дополнительные сведения см. в разделе [CDialog::D омодал](../../mfc/reference/cdialog-class.md#domodal).

### <a name="remarks"></a>Комментарии

Диалоговое окно Назначение сочетаний клавиш позволяет выбрать и назначить сочетания клавиш различным категориям команд. Кроме того, можно скопировать выбранные сочетания клавиш и их описание в буфер обмена.

## <a name="cmfckeymapdialogformatitem"></a><a name="formatitem"></a> Кмфккэймапдиалог:: Форматитем

Вызывается платформой для создания строки, описывающей сопоставление ключей. По умолчанию строка содержит имя команды, используемые сочетания клавиш и описание сочетания клавиш.

```
virtual CString FormatItem(int nItem) const;
```

### <a name="parameters"></a>Параметры

*нитем*<br/>
окне Отсчитываемый от нуля индекс элемента во внутреннем списке сопоставлений ключей.

### <a name="return-value"></a>Возвращаемое значение

`CString`Объект, содержащий текст форматированного элемента.

### <a name="remarks"></a>Комментарии

## <a name="cmfckeymapdialoggetcommandkeys"></a><a name="getcommandkeys"></a> Кмфккэймапдиалог:: Жеткоммандкэйс

Извлекает строковое значение. Строка содержит список сочетаний клавиш, связанных с указанной командой.

```
virtual CString GetCommandKeys(UINT uiCmdID) const;
```

### <a name="parameters"></a>Параметры

*уикмдид*<br/>
окне Идентификатор команды.

### <a name="return-value"></a>Возвращаемое значение

Разделенный точками с запятой список сочетаний клавиш, связанных с указанной командой.

### <a name="remarks"></a>Комментарии

## <a name="cmfckeymapdialogoninsertitem"></a><a name="oninsertitem"></a> Кмфккэймапдиалог:: Онинсертитем

Вызвано структурой перед вставкой нового элемента во внутренний элемент управления "список", поддерживающий элемент управления "сопоставление клавиш".

```
virtual void OnInsertItem(
    CMFCToolBarButton* pButton,
    int nItem);
```

### <a name="parameters"></a>Параметры

*пбуттон*<br/>
окне Указатель на кнопку панели инструментов, используемый для отображения сочетания клавиш с именем и описанием команды. Элемент схемы ключа хранится во внутреннем элементе управления "список".

*нитем*<br/>
окне Отсчитываемый от нуля индекс, указывающий место вставки нового элемента схемы ключа во внутренний элемент управления "список".

### <a name="remarks"></a>Комментарии

## <a name="cmfckeymapdialogonprintheader"></a><a name="onprintheader"></a> Кмфккэймапдиалог:: Онпринсеадер

Вызывается платформой для печати заголовка для схемы клавиатуры на новой странице.

```
virtual int OnPrintHeader(
    CDC& dc,
    int nPage,
    int cx) const;
```

### <a name="parameters"></a>Параметры

*dc*<br/>
окне Контекст устройства для принтера.

*нпаже*<br/>
окне Номер страницы для печати.

*/CX*<br/>
окне Горизонтальное смещение заголовка в пикселях.

### <a name="return-value"></a>Возвращаемое значение

В случае успеха высота напечатанного текста. Дополнительные сведения см. в разделе "возвращаемое значение" [CDC::D равтекст](../../mfc/reference/cdc-class.md#drawtext).

### <a name="remarks"></a>Комментарии

Платформа использует этот метод для печати схемы клавиатуры. По умолчанию этот метод выводит номер страницы, имя приложения и заголовок диалогового окна.

## <a name="cmfckeymapdialogonprintitem"></a><a name="onprintitem"></a> Кмфккэймапдиалог:: Онпринтитем

Вызывается платформой для печати элемента назначения клавиатуры.

```
virtual int OnPrintItem(
    CDC& dc,
    int nItem,
    int y,
    int cx,
    BOOL bCalcHeight) const;
```

### <a name="parameters"></a>Параметры

*dc*<br/>
окне Контекст устройства принтера.

*нитем*<br/>
окне Отсчитываемый от нуля индекс элемента для печати.

*y*<br/>
окне Вертикальное смещение между верхней границей страницы и позицией элемента.

*/CX*<br/>
окне Горизонтальное смещение слева от страницы и позиция элемента.

*бкалчеигхт*<br/>
окне Значение TRUE, чтобы вычислить наилучшую высоту элемента печати; Значение FALSE, чтобы усечь элемент печати, чтобы он соответствовал используемому по умолчанию пространству.

### <a name="return-value"></a>Возвращаемое значение

Высота напечатанного элемента.

### <a name="remarks"></a>Комментарии

Платформа вызывает этот метод для печати элемента диалогового окна "Таблица ключей". По умолчанию этот метод выводит имя команды, сочетания клавиш и описание команды элемента.

## <a name="cmfckeymapdialogonsetcolumns"></a><a name="onsetcolumns"></a> Кмфккэймапдиалог:: Онсетколумнс

Вызывается платформой для установки заголовков столбцов во внутреннем элементе управления "список", поддерживающем элемент управления "сопоставление клавиш".

```
virtual void OnSetColumns();
```

### <a name="remarks"></a>Комментарии

По умолчанию этот метод получает заголовки для столбцов из трех ресурсов. Заголовок столбца команд имеет IDS_AFXBARRES_COMMAND, заголовок ключевого столбца взят из IDS_AFXBARRES_KEYS, а заголовок столбца описания — из IDS_AFXBARRES_DESCRIPTION.

## <a name="cmfckeymapdialogprintkeymap"></a><a name="printkeymap"></a> Кмфккэймапдиалог::P Ринткэймап

Вызывается платформой при нажатии пользователем кнопки " **Печать** ".

```
virtual void PrintKeyMap();
```

### <a name="remarks"></a>Комментарии

`PrintKeyMap`Метод выводит карту ключей. Он инициирует новое задание печати, а затем повторно вызывает методы [кмфккэймапдиалог:: онпринсеадер](#onprintheader) и [Кмфккэймапдиалог:: онпринтитем](#onprintitem) до тех пор, пока не будут распечатаны все сопоставления ключей.

## <a name="cmfckeymapdialogsetcolumnswidth"></a><a name="setcolumnswidth"></a> Кмфккэймапдиалог:: Сетколумнсвидс

Вызывается платформой для установки ширины столбцов в элементе управления "внутренний список", поддерживающем элемент управления "сопоставление клавиш".

```
virtual void SetColumnsWidth();
```

### <a name="remarks"></a>Комментарии

Этот метод задает ширину по умолчанию для столбцов элемента управления "внутренний список". Во-первых, вычисляется ширина столбца сочетаний клавиш. Затем одна третья из оставшейся ширины выделяется для командного столбца, а оставшиеся две трети выделяются столбцу Description.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CKeyboardManager](../../mfc/reference/ckeyboardmanager-class.md)
