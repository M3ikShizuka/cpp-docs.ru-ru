---
description: 'Дополнительные сведения о: структура CPrintInfo'
title: Структура CPrintInfo
ms.date: 11/04/2016
f1_keywords:
- CPrintInfo
helpviewer_keywords:
- CPrintInfo structure [MFC]
ms.assetid: 0b3de849-d050-4386-9a14-f4c1a25684f7
ms.openlocfilehash: 355bcf2f04b32756ae16147465054e945d70cf78
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97343392"
---
# <a name="cprintinfo-structure"></a>Структура CPrintInfo

Хранит сведения о задании печати или печати.

## <a name="syntax"></a>Синтаксис

```
struct CPrintInfo
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CPrintInfo:: Жетфромпаже](#getfrompage)|Возвращает номер первой печатаемой страницы.|
|[CPrintInfo:: Жетмакспаже](#getmaxpage)|Возвращает номер последней страницы документа.|
|[CPrintInfo:: Жетминпаже](#getminpage)|Возвращает номер первой страницы документа.|
|[CPrintInfo:: Жетоффсетпаже](#getoffsetpage)|Возвращает число страниц, предшествующих первой странице DocObject элемента, выводимых в объединенном задании печати DocObject.|
|[CPrintInfo:: Жеттопаже](#gettopage)|Возвращает номер последней печатаемой страницы.|
|[CPrintInfo:: Сетмакспаже](#setmaxpage)|Задает номер последней страницы документа.|
|[CPrintInfo:: Сетминпаже](#setminpage)|Задает номер первой страницы документа.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[CPrintInfo:: m_bContinuePrinting](#m_bcontinueprinting)|Содержит флаг, указывающий, должна ли платформа продолжить цикл печати.|
|[CPrintInfo:: m_bDirect](#m_bdirect)|Содержит флаг, указывающий, выполняется ли печать документа напрямую (без отображения диалогового окна Печать).|
|[CPrintInfo:: m_bDocObject](#m_bdocobject)|Содержит флаг, указывающий, является ли печатаемый документ DocObject.|
|[CPrintInfo:: m_bPreview](#m_bpreview)|Содержит флаг, указывающий, выполняется ли предварительный просмотр документа.|
|[CPrintInfo:: m_dwFlags](#m_dwflags)|Указывает операции печати DocObject.|
|[CPrintInfo:: m_lpUserData](#m_lpuserdata)|Содержит указатель на структуру, созданную пользователем.|
|[CPrintInfo:: m_nCurPage](#m_ncurpage)|Определяет номер страницы, которая печатается в данный момент.|
|[CPrintInfo:: m_nJobNumber](#m_njobnumber)|Указывает номер задания, назначенный операционной системой для текущего задания печати|
|[CPrintInfo:: m_nNumPreviewPages](#m_nnumpreviewpages)|Определяет количество страниц, отображаемых в окне предварительного просмотра; 1 или 2.|
|[CPrintInfo:: m_nOffsetPage](#m_noffsetpage)|Указывает смещение первой страницы DocObject в объединенном задании печати DocObject.|
|[CPrintInfo:: m_pPD](#m_ppd)|Содержит указатель на объект, `CPrintDialog` используемый для диалогового окна «Печать».|
|[CPrintInfo:: m_rectDraw](#m_rectdraw)|Задает прямоугольник, определяющий текущую используемую область страницы.|
|[CPrintInfo:: m_strPageDesc](#m_strpagedesc)|Содержит строку формата для вывода номера страницы.|

## <a name="remarks"></a>Комментарии

`CPrintInfo` является структурой и не имеет базового класса.

Платформа создает объект `CPrintInfo` каждый раз, когда выбрана команда печати или предварительного просмотра печати, и удаляет ее после завершения команды.

`CPrintInfo` содержит сведения о задании печати в целом, например диапазон печатаемых страниц, а также текущее состояние задания печати, например печать страницы в данный момент. Некоторые сведения хранятся в связанном объекте [кпринтдиалог](../../mfc/reference/cprintdialog-class.md) . Этот объект содержит значения, указанные пользователем в диалоговом окне «Печать».

`CPrintInfo`Объект передается между платформой и классом представления во время процесса печати и используется для обмена данными между ними. Например, платформа сообщает классу представления, какую страницу документа следует напечатать, присваивая значение `m_nCurPage` члену `CPrintInfo` ; класс view извлекает значение и выполняет фактическую печать указанной страницы.

Другой пример — ситуация, в которой длина документа неизвестна до вывода на печать. В этом случае класс представления проверяет конец документа при каждой печати страницы. При достижении конца класс представления устанавливает `m_bContinuePrinting` `CPrintInfo` для члена значение false; это указывает платформе на необходимость прекратить цикл печати.

`CPrintInfo` используется функциями-членами, `CView` перечисленными в разделе "см. также". Дополнительные сведения об архитектуре печати, предоставляемой библиотека Microsoft Foundation Class, см. в разделах окна и [документ/представление](../../mfc/document-view-architecture.md) в [рамке](../../mfc/frame-windows.md) , а также [Печать](../../mfc/printing.md) и [Печать статей: многостраничные документы](../../mfc/multipage-documents.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CPrintInfo`

## <a name="requirements"></a>Требования

**Заголовок:** афксекст. h

## <a name="cprintinfogetfrompage"></a><a name="getfrompage"></a> CPrintInfo:: Жетфромпаже

Вызовите эту функцию, чтобы получить номер первой страницы для печати.

```
UINT GetFromPage() const;
```

### <a name="return-value"></a>Возвращаемое значение

Номер первой страницы, которая будет напечатана.

### <a name="remarks"></a>Комментарии

Это значение, указанное пользователем в диалоговом окне «Печать», сохраняется в `CPrintDialog` объекте, на который ссылается `m_pPD` элемент. Если пользователь не указал значение, по умолчанию используется первая страница документа.

## <a name="cprintinfogetmaxpage"></a><a name="getmaxpage"></a> CPrintInfo:: Жетмакспаже

Вызовите эту функцию, чтобы получить номер последней страницы документа.

```
UINT GetMaxPage() const;
```

### <a name="return-value"></a>Возвращаемое значение

Номер последней страницы документа.

### <a name="remarks"></a>Комментарии

Это значение хранится в `CPrintDialog` объекте, на который ссылается `m_pPD` член.

## <a name="cprintinfogetminpage"></a><a name="getminpage"></a> CPrintInfo:: Жетминпаже

Вызовите эту функцию, чтобы получить номер первой страницы документа.

```
UINT GetMinPage() const;
```

### <a name="return-value"></a>Возвращаемое значение

Номер первой страницы документа.

### <a name="remarks"></a>Комментарии

Это значение хранится в `CPrintDialog` объекте, на который ссылается `m_pPD` член.

## <a name="cprintinfogetoffsetpage"></a><a name="getoffsetpage"></a> CPrintInfo:: Жетоффсетпаже

Вызовите эту функцию, чтобы получить смещение при печати нескольких элементов DocObject из клиента DocObject.

```
UINT GetOffsetPage() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число страниц, предшествующих первой странице элемента DocObject, печатаемых в объединенном задании печати DocObject.

### <a name="remarks"></a>Комментарии

На это значение ссылается `m_nOffsetPage` элемент. На первой странице документа будет пронумеровано `m_nOffsetPage` значение + 1 при печати в виде DocObject с другими активными документами. `m_nOffsetPage`Элемент допустим только в том случае, если `m_bDocObject` значение равно true.

## <a name="cprintinfogettopage"></a><a name="gettopage"></a> CPrintInfo:: Жеттопаже

Вызовите эту функцию, чтобы получить номер последней страницы для печати.

```
UINT GetToPage() const;
```

### <a name="return-value"></a>Возвращаемое значение

Номер последней выводимой страницы.

### <a name="remarks"></a>Комментарии

Это значение, указанное пользователем в диалоговом окне «Печать», сохраняется в `CPrintDialog` объекте, на который ссылается `m_pPD` элемент. Если пользователь не указал значение, по умолчанию используется последняя страница документа.

## <a name="cprintinfom_bcontinueprinting"></a><a name="m_bcontinueprinting"></a> CPrintInfo:: m_bContinuePrinting

Содержит флаг, указывающий, должна ли платформа продолжить цикл печати.

### <a name="remarks"></a>Комментарии

Если выполняется разбивка на страницы во время печати, можно задать для этого члена значение FALSE в переопределении `CView::OnPrepareDC` после достижения конца документа. Нет необходимости изменять эту переменную, если вы указали длину документа в начале задания печати с помощью `SetMaxPage` функции члена. `m_bContinuePrinting`Член является открытой переменной типа bool.

## <a name="cprintinfom_bdirect"></a><a name="m_bdirect"></a> CPrintInfo:: m_bDirect

Платформа присваивает этому элементу значение TRUE, если диалоговое окно печать будет пропущено для прямой печати; В противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Обычно диалоговое окно печати обходится при печати из оболочки или при завершении печати с помощью идентификатора команды ID_FILE_PRINT_DIRECT.

Обычно этот элемент не изменяется, но, если он изменяется, измените его перед вызовом [CView::D опрепарепринтинг](../../mfc/reference/cview-class.md#doprepareprinting) в переопределении [CView:: онпрепарепринтинг](../../mfc/reference/cview-class.md#onprepareprinting).

## <a name="cprintinfom_bdocobject"></a><a name="m_bdocobject"></a> CPrintInfo:: m_bDocObject

Содержит флаг, указывающий, является ли печатаемый документ DocObject.

### <a name="remarks"></a>Комментарии

Элементы данных `m_dwFlags` и `m_nOffsetPage` являются недопустимыми, если этот флаг не равен true.

## <a name="cprintinfom_bpreview"></a><a name="m_bpreview"></a> CPrintInfo:: m_bPreview

Содержит флаг, указывающий, выполняется ли предварительный просмотр документа.

### <a name="remarks"></a>Комментарии

Это значение задается платформой в зависимости от выполняемой пользователем команды. Диалоговое окно «печать» не отображается для задания «Печать-просмотр». `m_bPreview`Член является открытой переменной типа bool.

## <a name="cprintinfom_dwflags"></a><a name="m_dwflags"></a> CPrintInfo:: m_dwFlags

Содержит сочетание флагов, определяющих операции печати DocObject.

### <a name="remarks"></a>Комментарии

Допустим, только если элемент данных `m_bDocObject` имеет значение true.

Флагами может быть одно или несколько из следующих значений:

- PRINTFLAG_MAYBOTHERUSER

- PRINTFLAG_PROMPTUSER

- PRINTFLAG_USERMAYCHANGEPRINTER

- PRINTFLAG_RECOMPOSETODEVICE

- PRINTFLAG_DONTACTUALLYPRINT

- PRINTFLAG_FORCEPROPERTIES

- PRINTFLAG_PRINTTOFILE

## <a name="cprintinfom_lpuserdata"></a><a name="m_lpuserdata"></a> CPrintInfo:: m_lpUserData

Содержит указатель на структуру, созданную пользователем.

### <a name="remarks"></a>Комментарии

Его можно использовать для хранения данных, относящихся к печати, которые не нужно хранить в классе представления. `m_lpUserData`Член является открытой переменной типа лпвоид.

## <a name="cprintinfom_ncurpage"></a><a name="m_ncurpage"></a> CPrintInfo:: m_nCurPage

Содержит номер текущей страницы.

### <a name="remarks"></a>Комментарии

Платформа вызывает `CView::OnPrepareDC` и `CView::OnPrint` один раз для каждой страницы документа, одновременно указывая различные значения для этого элемента; его значения изменяются, начиная со значения `GetFromPage` , возвращаемого методом `GetToPage` . Используйте этот член в переопределениях `CView::OnPrepareDC` и `CView::OnPrint` для печати указанной страницы документа.

При первом вызове режима предварительного просмотра платформа считывает значение этого элемента, чтобы определить, какая страница документа должна быть предварительно просматриваема. Можно задать значение этого члена в переопределении, `CView::OnPreparePrinting` чтобы сохранить текущую позицией пользователя в документе при переходе в режим предварительного просмотра. `m_nCurPage`Член является открытой переменной типа uint.

## <a name="cprintinfom_njobnumber"></a><a name="m_njobnumber"></a> CPrintInfo:: m_nJobNumber

Указывает номер задания, назначенный операционной системой для текущего задания печати.

### <a name="remarks"></a>Комментарии

Это значение может быть SP_ERROR, если задание еще не напечатано (то есть, если `CPrintInfo` объект создан заново и еще не использовался для печати) или если при запуске задания произошла ошибка.

## <a name="cprintinfom_nnumpreviewpages"></a><a name="m_nnumpreviewpages"></a> CPrintInfo:: m_nNumPreviewPages

Содержит количество страниц, отображаемых в режиме предварительного просмотра. может иметь значение 1 или 2.

### <a name="remarks"></a>Комментарии

`m_nNumPreviewPages`Член является открытой переменной типа uint.

## <a name="cprintinfom_noffsetpage"></a><a name="m_noffsetpage"></a> CPrintInfo:: m_nOffsetPage

Содержит число страниц, предшествующих первой странице определенного DocObject в объединенном задании печати DocObject.

## <a name="cprintinfom_ppd"></a><a name="m_ppd"></a> CPrintInfo:: m_pPD

Содержит указатель на объект, `CPrintDialog` используемый для отображения диалогового окна «Печать» для задания печати.

### <a name="remarks"></a>Комментарии

`m_pPD`Член является открытой переменной, объявленной как указатель на `CPrintDialog` .

## <a name="cprintinfom_rectdraw"></a><a name="m_rectdraw"></a> CPrintInfo:: m_rectDraw

Указывает используемую область рисования страницы в логических координатах.

### <a name="remarks"></a>Комментарии

Это можно сделать в переопределении `CView::OnPrint` . Этот элемент можно использовать для наблюдения за тем, какие области остаются пригодными для использования после печати заголовков, нижних колонтитулов и т. д. `m_rectDraw`Член является открытой переменной типа `CRect` .

## <a name="cprintinfom_strpagedesc"></a><a name="m_strpagedesc"></a> CPrintInfo:: m_strPageDesc

Содержит строку форматирования, используемую для отображения номеров страниц во время предварительного просмотра. Эта строка состоит из двух подстрок: одна для одностраничного вывода, а другая — для вывода двойной страницы, каждая из которых завершается символом "\n".

### <a name="remarks"></a>Комментарии

Платформа использует значение "Page%У\нпажес% u-%у\н" в качестве значения по умолчанию. Если требуется другой формат номеров страниц, укажите строку формата в переопределении `CView::OnPreparePrinting` . `m_strPageDesc`Член является открытой переменной типа `CString` .

## <a name="cprintinfosetmaxpage"></a><a name="setmaxpage"></a> CPrintInfo:: Сетмакспаже

Вызовите эту функцию, чтобы указать номер последней страницы документа.

```cpp
void SetMaxPage(UINT nMaxPage);
```

### <a name="parameters"></a>Параметры

*нмакспаже*<br/>
Номер последней страницы документа.

### <a name="remarks"></a>Комментарии

Это значение хранится в `CPrintDialog` объекте, на который ссылается `m_pPD` член. Если длина документа известна до вывода на печать, вызовите эту функцию из переопределения `CView::OnPreparePrinting` . Если длина документа зависит от параметра, указанного пользователем в диалоговом окне Печать, вызовите эту функцию из переопределения `CView::OnBeginPrinting` . Если длина документа неизвестна до вывода на печать, используйте `m_bContinuePrinting` элемент для управления циклом печати.

### <a name="example"></a>Пример

  См. пример для [CView:: онпрепарепринтинг](../../mfc/reference/cview-class.md#onprepareprinting).

## <a name="cprintinfosetminpage"></a><a name="setminpage"></a> CPrintInfo:: Сетминпаже

Вызовите эту функцию, чтобы указать номер первой страницы документа.

```cpp
void SetMinPage(UINT nMinPage);
```

### <a name="parameters"></a>Параметры

*нминпаже*<br/>
Номер первой страницы документа.

### <a name="remarks"></a>Комментарии

Номера страниц обычно начинаются с 1. Это значение хранится в `CPrintDialog` объекте, на который ссылается `m_pPD` член.

## <a name="see-also"></a>См. также раздел

[Пример DIBLOOK в MFC](../../overview/visual-cpp-samples.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[CView::OnBeginPrinting](../../mfc/reference/cview-class.md#onbeginprinting)<br/>
[CView:: Онендпринтинг](../../mfc/reference/cview-class.md#onendprinting)<br/>
[CView:: Онендпринтпревиев](../../mfc/reference/cview-class.md#onendprintpreview)<br/>
[CView:: Онпрепаредк](../../mfc/reference/cview-class.md#onpreparedc)<br/>
[CView:: Онпрепарепринтинг](../../mfc/reference/cview-class.md#onprepareprinting)<br/>
[CView:: OnPrint](../../mfc/reference/cview-class.md#onprint)
