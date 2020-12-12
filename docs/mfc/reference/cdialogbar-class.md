---
description: 'Дополнительные сведения о: CDialogBar Class'
title: Класс CDialogBar
ms.date: 11/04/2016
f1_keywords:
- CDialogBar
- AFXEXT/CDialogBar
- AFXEXT/CDialogBar::CDialogBar
- AFXEXT/CDialogBar::Create
helpviewer_keywords:
- CDialogBar [MFC], CDialogBar
- CDialogBar [MFC], Create
ms.assetid: da2f7a30-970c-44e3-87f0-6094bd002cab
ms.openlocfilehash: 7feb31cd8152309557a398f5c8d0edb8d91c340e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185223"
---
# <a name="cdialogbar-class"></a>Класс CDialogBar

Предоставляет функциональные возможности немодального диалогового окна Windows на панели элементов управления.

## <a name="syntax"></a>Синтаксис

```
class CDialogBar : public CControlBar
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CDialogBar:: CDialogBar](#cdialogbar)|Формирует объект `CDialogBar`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CDialogBar:: Create](#create)|Создает диалоговую панель Windows и прикрепляет ее к `CDialogBar` объекту.|

## <a name="remarks"></a>Комментарии

Диалоговая панель напоминает диалоговое окно, в котором он содержит стандартные элементы управления Windows, которые пользователь может выполнять на вкладке. Еще одним сходством является создание шаблона диалогового окна для представления диалоговой панели.

Создание и использование диалоговой панели аналогично созданию и использованию `CFormView` объекта. Во-первых, используйте [Редактор диалоговых окон](../../windows/dialog-editor.md) , чтобы определить шаблон диалогового окна с WS_CHILD стиля и без другого стиля. Шаблон не должен иметь WS_VISIBLE стиля. В коде приложения вызовите конструктор для создания `CDialogBar` объекта, а затем вызовите, `Create` чтобы создать окно диалогового окна и присоединить его к `CDialogBar` объекту.

Дополнительные сведения о см `CDialogBar` . в разделе панели [диалоговых](../../mfc/dialog-bars.md) окон и [Технические примечания 31](../../mfc/tn031-control-bars.md), панели управления.

> [!NOTE]
> В текущем выпуске `CDialogBar` объект не может содержать элементы управления Windows Forms. Дополнительные сведения об элементах управления Windows Forms в Visual C++ см. в разделе [Использование пользовательского элемента управления формы Windows в MFC](../../dotnet/using-a-windows-form-user-control-in-mfc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CControlBar](../../mfc/reference/ccontrolbar-class.md)

`CDialogBar`

## <a name="requirements"></a>Требования

**Заголовок:** афксекст. h

## <a name="cdialogbarcdialogbar"></a><a name="cdialogbar"></a> CDialogBar:: CDialogBar

Формирует объект `CDialogBar`.

```
CDialogBar();
```

## <a name="cdialogbarcreate"></a><a name="create"></a> CDialogBar:: Create

Загружает шаблон ресурсов диалогового окна, указанный параметром `lpszTemplateName` или `nIDTemplate` , создает окно диалогового окна, устанавливает его стиль и связывает с `CDialogBar` объектом.

```
virtual BOOL Create(
    CWnd* pParentWnd,
    LPCTSTR lpszTemplateName,
    UINT nStyle,
    UINT nID);

virtual BOOL Create(
    CWnd* pParentWnd,
    UINT nIDTemplate,
    UINT nStyle,
    UINT nID);
```

### <a name="parameters"></a>Параметры

*ппарентвнд*<br/>
Указатель на родительский `CWnd` объект.

*лпсзтемплатенаме*<br/>
Указатель на имя `CDialogBar` шаблона ресурсов диалогового окна объекта.

*nStyle*<br/>
Стиль панели инструментов. Поддерживаются следующие дополнительные стили панелей инструментов:

- Панель управления CBRS_TOP находится в верхней части окна фрейма.

- Панель управления CBRS_BOTTOM находится в нижней части окна фрейма.

- CBRS_NOALIGN панель управления не перемещается при изменении размера родительского элемента.

- В панели управления CBRS_TOOLTIPS отображаются подсказки.

- Панель управления CBRS_SIZE_DYNAMIC является динамической.

- Панель управления CBRS_SIZE_FIXED фиксирована.

- CBRS_FLOATING панель управления является плавающей.

- Строка состояния CBRS_FLYBY отображает сведения о кнопке.

- Панель управления CBRS_HIDE_INPLACE не отображается для пользователя.

*nID*<br/>
Идентификатор элемента управления диалоговой панели.

*нидтемплате*<br/>
Идентификатор ресурса для `CDialogBar` шаблона диалогового окна объекта.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Если задать стиль выравнивания CBRS_TOP или CBRS_BOTTOM, то ширина диалогового окна будет равна ширине окна фрейма и его высотой, то есть ресурса, заданного параметром *нидтемплате*. Если задать стиль выравнивания CBRS_LEFT или CBRS_RIGHT, то высота диалогового окна будет равна, так как окно фрейма и его ширина — это ресурс, заданный параметром *нидтемплате*.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCMessageMaps#13](../../mfc/reference/codesnippet/cpp/cdialogbar-class_1.cpp)]

## <a name="see-also"></a>См. также раздел

[Пример CTRLBARS в MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс CControlBar](../../mfc/reference/ccontrolbar-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CFormView](../../mfc/reference/cformview-class.md)<br/>
[Класс CControlBar](../../mfc/reference/ccontrolbar-class.md)
