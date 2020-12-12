---
description: Дополнительные сведения о классе "CFormView"
title: Класс CFormView
ms.date: 11/04/2016
f1_keywords:
- CFormView
- AFXEXT/CFormView
- AFXEXT/CFormView::CFormView
- AFXEXT/CFormView::IsInitDlgCompleted
helpviewer_keywords:
- CFormView [MFC], CFormView
- CFormView [MFC], IsInitDlgCompleted
ms.assetid: a99ec313-36f0-4f28-9d2b-de11de14ac19
ms.openlocfilehash: ec37a3819f299830fef96bfdf93c0170b2969c66
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97184313"
---
# <a name="cformview-class"></a>Класс CFormView

Базовый класс, используемый для представлений формы.

## <a name="syntax"></a>Синтаксис

```
class CFormView : public CScrollView
```

## <a name="members"></a>Члены

### <a name="protected-constructors"></a>Защищенные конструкторы

|Имя|Описание|
|----------|-----------------|
|[CFormView::CFormView](#cformview)|Формирует объект `CFormView`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CFormView::IsInitDlgCompleted](#isinitdlgcompleted)|Используется для синхронизации во время инициализации.|

## <a name="remarks"></a>Комментарии

По сути, представление формы — это представление, содержащее элементы управления. Эти элементы управления располагаются на основе ресурса шаблона диалогового окна. Используйте `CFormView`, если вы хотите задействовать формы в своем приложении. Эти представления поддерживают прокрутку при необходимости с помощью функции [кскроллвиев](../../mfc/reference/cscrollview-class.md) .

При [создании Forms-Basedного приложения](../../mfc/reference/creating-a-forms-based-mfc-application.md)можно создать его класс представления на `CFormView` основе, сделав его приложением, основанным на формах.

Можно также вставлять новые [разделы форм](../../mfc/form-views-mfc.md) в приложения на основе представления документа. Даже если ваше приложение изначально не поддерживает формы, при вставке новой формы Visual C++ обеспечит их поддержку.

Приложения на основе форм рекомендуется создавать с помощью мастера приложений MFC и команды Add Class. Если необходимо создать приложение на основе форм без использования этих методов, см. раздел [создание Forms-Based приложения](../../mfc/reference/creating-a-forms-based-mfc-application.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CView](../../mfc/reference/cview-class.md)

[CScrollView](../../mfc/reference/cscrollview-class.md)

`CFormView`

## <a name="requirements"></a>Требования

**Заголовок:** афксекст. h

## <a name="cformviewcformview"></a><a name="cformview"></a> CFormView:: CFormView

Формирует объект `CFormView`.

```
CFormView(LPCTSTR lpszTemplateName);
CFormView(UINT nIDTemplate);
```

### <a name="parameters"></a>Параметры

*лпсзтемплатенаме*<br/>
Содержит строку, завершающуюся нулем, которая является именем ресурса шаблона диалогового окна.

*нидтемплате*<br/>
Содержит ИДЕНТИФИКАЦИОНный номер ресурса шаблона диалогового окна.

### <a name="remarks"></a>Комментарии

При создании объекта типа, производного от `CFormView` , вызовите один из конструкторов для создания объекта представления и укажите ресурс диалогового окна, на котором основано представление. Ресурс можно указать по имени (передать строку в качестве аргумента в конструктор) или по его ИДЕНТИФИКАТОРу (передайте в качестве аргумента целое число без знака).

Окно представления формы и дочерние элементы управления не создаются до тех пор, пока `CWnd::Create` не будет вызван метод. `CWnd::Create` вызывается платформой как часть документа и процесса создания представления, который определяется шаблоном документа.

> [!NOTE]
> Производный класс *должен* предоставить собственный конструктор. В конструкторе вызовите конструктор, `CFormView::CFormView` с именем ресурса или идентификатором в качестве аргумента, как показано в предыдущем обзоре класса.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCDocView#90](../../mfc/codesnippet/cpp/cformview-class_1.h)]

[!code-cpp[NVC_MFCDocView#91](../../mfc/codesnippet/cpp/cformview-class_2.cpp)]

## <a name="cformviewisinitdlgcompleted"></a><a name="isinitdlgcompleted"></a> CFormView:: Исинитдлгкомплетед

Используется MFC, чтобы убедиться, что инициализация завершена до выполнения других операций.

```
BOOL IsInitDlgCompleted() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если инициализация для этого диалогового окна была завершена.

## <a name="see-also"></a>См. также раздел

[Пример СНАПВВ для MFC](../../overview/visual-cpp-samples.md)<br/>
[Пример примера VIEWEX MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс Кскроллвиев](../../mfc/reference/cscrollview-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CDialog](../../mfc/reference/cdialog-class.md)<br/>
[Класс Кскроллвиев](../../mfc/reference/cscrollview-class.md)
