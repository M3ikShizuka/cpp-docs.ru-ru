---
description: 'Дополнительные сведения о: Кмултипажедхтмлдиалог Class'
title: Класс Кмултипажедхтмлдиалог
ms.date: 03/27/2019
f1_keywords:
- CMultiPageDHtmlDialog
- AFXDHTML/CMultiPageDHtmlDialog
- AFXDHTML/CMultiPageDHtmlDialog::CMultiPageDHtmlDialog
helpviewer_keywords:
- CMultiPageDHtmlDialog [MFC], CMultiPageDHtmlDialog
ms.assetid: 971accc1-824d-4df4-b4c1-b1a20e0f7e4f
ms.openlocfilehash: 1f7f8c2081687c71a98e427bb5396cfa47a73deb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331530"
---
# <a name="cmultipagedhtmldialog-class"></a>Класс Кмултипажедхтмлдиалог

Многостраничное диалоговое окно последовательно отображает несколько HTML-страниц и обрабатывает события каждой страницы.

## <a name="syntax"></a>Синтаксис

```
class CMultiPageDHtmlDialog : public CDHtmlDialog
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмултипажедхтмлдиалог:: Кмултипажедхтмлдиалог](#cmultipagedhtmldialog)|Конструирует многостраничный (в стиле мастера) объект диалогового окна DHTML.|
|[Кмултипажедхтмлдиалог:: ~ Кмултипажедхтмлдиалог](#_dtorcmultipagedhtmldialog)|Уничтожает многостраничный объект диалогового окна DHTML.|

## <a name="remarks"></a>Комментарии

Этот механизм является [сопоставлением событий DHTML и URL-адресов](dhtml-event-maps.md), который содержит внедренные карты событий для каждой страницы.

## <a name="example"></a>Пример

В этом многостраничном диалоговом окне предполагается три HTML-ресурса, определяющие простые функции, аналогичные мастеру. На первой странице имеется кнопка **Далее** , вторая кнопка **назад** и **Далее** , а также третья кнопка **назад** . При нажатии одной из кнопок функция обработчика вызывает [CDHtmlDialog:: лоадфромресаурце](../../mfc/reference/cdhtmldialog-class.md#loadfromresource) для загрузки соответствующей новой страницы.

Соответствующие части объявления класса (в Кмимултипажедлг. h):

[!code-cpp[NVC_MFCDocView#181](../../mfc/codesnippet/cpp/cmultipagedhtmldialog-class_1.h)]

Соответствующие части реализации класса (в Кмимултипажедлг. cpp):

[!code-cpp[NVC_MFCDocView#182](../../mfc/codesnippet/cpp/cmultipagedhtmldialog-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CDHtmlSinkHandlerBase2`

`CDHtmlSinkHandlerBase1`

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

`CDHtmlSinkHandler`

[CWnd](../../mfc/reference/cwnd-class.md)

`CDHtmlEventSink`

[CDialog](../../mfc/reference/cdialog-class.md)

[CDHtmlDialog](../../mfc/reference/cdhtmldialog-class.md)

`CMultiPageDHtmlDialog`

## <a name="requirements"></a>Требования

**Заголовок:** афксдхтмл. h

## <a name="cmultipagedhtmldialogcmultipagedhtmldialog"></a><a name="cmultipagedhtmldialog"></a> Кмултипажедхтмлдиалог:: Кмултипажедхтмлдиалог

Конструирует многостраничный (в стиле мастера) объект диалогового окна DHTML.

```
CMultiPageDHtmlDialog(
    LPCTSTR lpszTemplateName,
    LPCTSTR szHtmlResID = NULL,
    CWnd* pParentWnd = NULL);

CMultiPageDHtmlDialog(
    UINT nIDTemplate,
    UINT nHtmlResID = 0,
    CWnd* pParentWnd = NULL);

CMultiPageDHtmlDialog();
```

### <a name="parameters"></a>Параметры

*лпсзтемплатенаме*<br/>
Строка, завершающаяся нулем, которая является именем ресурса шаблона диалогового окна.

*сзтмлресид*<br/>
Строка, завершающаяся нулем, которая является именем ресурса HTML.

*ппарентвнд*<br/>
Указатель на родительский или объект окна-владельца (типа [CWnd](../../mfc/reference/cwnd-class.md)), которому принадлежит объект диалогового окна. Если значение равно NULL, то родительское окно объекта диалогового окна устанавливается в главное окно приложения.

*нидтемплате*<br/>
Содержит ИДЕНТИФИКАЦИОНный номер ресурса шаблона диалогового окна.

*нхтмлресид*<br/>
Содержит ИДЕНТИФИКАЦИОНный номер ресурса HTML.

## <a name="cmultipagedhtmldialogcmultipagedhtmldialog"></a><a name="_dtorcmultipagedhtmldialog"></a> Кмултипажедхтмлдиалог:: ~ Кмултипажедхтмлдиалог

Уничтожает многостраничный объект диалогового окна DHTML.

```
virtual ~CMultiPageDHtmlDialog();
```

## <a name="see-also"></a>См. также раздел

[Класс CDHtmlDialog](../../mfc/reference/cdhtmldialog-class.md)
