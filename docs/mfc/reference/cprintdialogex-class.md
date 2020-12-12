---
description: 'Дополнительные сведения о: Кпринтдиаложекс Class'
title: Класс Кпринтдиаложекс
ms.date: 11/04/2016
f1_keywords:
- CPrintDialogEx
- AFXDLGS/CPrintDialogEx
- AFXDLGS/CPrintDialogEx::CPrintDialogEx
- AFXDLGS/CPrintDialogEx::CreatePrinterDC
- AFXDLGS/CPrintDialogEx::DoModal
- AFXDLGS/CPrintDialogEx::GetCopies
- AFXDLGS/CPrintDialogEx::GetDefaults
- AFXDLGS/CPrintDialogEx::GetDeviceName
- AFXDLGS/CPrintDialogEx::GetDevMode
- AFXDLGS/CPrintDialogEx::GetDriverName
- AFXDLGS/CPrintDialogEx::GetPortName
- AFXDLGS/CPrintDialogEx::GetPrinterDC
- AFXDLGS/CPrintDialogEx::PrintAll
- AFXDLGS/CPrintDialogEx::PrintCollate
- AFXDLGS/CPrintDialogEx::PrintCurrentPage
- AFXDLGS/CPrintDialogEx::PrintRange
- AFXDLGS/CPrintDialogEx::PrintSelection
- AFXDLGS/CPrintDialogEx::m_pdex
helpviewer_keywords:
- CPrintDialogEx [MFC], CPrintDialogEx
- CPrintDialogEx [MFC], CreatePrinterDC
- CPrintDialogEx [MFC], DoModal
- CPrintDialogEx [MFC], GetCopies
- CPrintDialogEx [MFC], GetDefaults
- CPrintDialogEx [MFC], GetDeviceName
- CPrintDialogEx [MFC], GetDevMode
- CPrintDialogEx [MFC], GetDriverName
- CPrintDialogEx [MFC], GetPortName
- CPrintDialogEx [MFC], GetPrinterDC
- CPrintDialogEx [MFC], PrintAll
- CPrintDialogEx [MFC], PrintCollate
- CPrintDialogEx [MFC], PrintCurrentPage
- CPrintDialogEx [MFC], PrintRange
- CPrintDialogEx [MFC], PrintSelection
- CPrintDialogEx [MFC], m_pdex
ms.assetid: 1d506703-ee1c-44cc-b4ce-4e778fec26b8
ms.openlocfilehash: 2f0d124422efa641c3ace833a5970b364a5cbc48
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97301468"
---
# <a name="cprintdialogex-class"></a>Класс Кпринтдиаложекс

Инкапсулирует службы, предоставляемые страницей свойств печати Windows.

## <a name="syntax"></a>Синтаксис

```
class CPrintDialogEx : public CCommonDialog
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кпринтдиаложекс:: Кпринтдиаложекс](#cprintdialogex)|Формирует объект `CPrintDialogEx`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кпринтдиаложекс:: Креатепринтердк](#createprinterdc)|Создает контекст печатающего устройства, не отображая диалоговое окно Печать.|
|[Кпринтдиаложекс::D Омодал](#domodal)|Отображает диалоговое окно и позволяет пользователю выбрать нужные элементы.|
|[Кпринтдиаложекс:: выполняет копирование](#getcopies)|Возвращает количество запрошенных копий.|
|[Кпринтдиаложекс:: параметры по умолчанию](#getdefaults)|Извлекает значения по умолчанию для устройств без отображения диалогового окна.|
|[Кпринтдиаложекс:: Жетдевиценаме](#getdevicename)|Извлекает имя выбранного в данный момент принтера.|
|[Кпринтдиаложекс::](#getdevmode)|Извлекает `DEVMODE` структуру.|
|[Кпринтдиаложекс:: GetDriverName](#getdrivername)|Возвращает имя драйвера устройства печати, определенного системой.|
|[Кпринтдиаложекс:: Жетпортнаме](#getportname)|Извлекает имя выбранного в данный момент порта принтера.|
|[Кпринтдиаложекс:: Жетпринтердк](#getprinterdc)|Извлекает маркер контекста устройства принтера.|
|[Кпринтдиаложекс::P Ринталл](#printall)|Определяет, следует ли печатать все страницы документа.|
|[Кпринтдиаложекс::P Ринтколлате](#printcollate)|Определяет, запрашиваются ли копии по копиям.|
|[Кпринтдиаложекс::P Ринткуррентпаже](#printcurrentpage)|Определяет, следует ли печатать текущую страницу документа.|
|[Кпринтдиаложекс::P Ринтранже](#printrange)|Определяет, следует ли печатать только указанный диапазон страниц.|
|[Кпринтдиаложекс::P Ринтселектион](#printselection)|Определяет, следует ли печатать только выбранные в данный момент элементы.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Кпринтдиаложекс:: m_pdex](#m_pdex)|Структура, используемая для настройки `CPrintDialogEx` объекта.|

## <a name="remarks"></a>Комментарии

Вы можете использовать платформу для обработки многих аспектов процесса печати приложения. Дополнительные сведения об использовании платформы для работы с задачами печати см. в статье [Печать](../../mfc/printing.md).

Если вы хотите, чтобы приложение обрабатывал печать без участия в платформе, можно использовать `CPrintDialogEx` класс "как есть" с предоставленным конструктором или создать собственный класс диалогового окна из `CPrintDialogEx` и написать конструктор в соответствии с вашими потребностями. В любом случае эти диалоговые окна будут вести себя так же, как стандартные диалоговые окна MFC, поскольку они являются производными от класса `CCommonDialog` .

Чтобы использовать `CPrintDialogEx` объект, сначала создайте объект с помощью `CPrintDialogEx` конструктора. После создания диалогового окна можно задать или изменить любые значения в структуре [m_pdex](#m_pdex) , чтобы инициализировать значения элементов управления диалогового окна. `m_pdex`Структура имеет тип [принтдлжекс](/windows/win32/api/commdlg/ns-commdlg-printdlgexw). Дополнительные сведения об этой структуре см. в Windows SDK.

Если вы не предоставляете собственные дескрипторы `m_pdex` для `hDevMode` `hDevNames` членов и, не забудьте вызвать функцию Windows `GlobalFree` для этих дескрипторов после завершения работы с диалоговым окном.

После инициализации элементов управления диалогового окна вызовите `DoModal` функцию члена, чтобы открыть диалоговое окно и позволить пользователю выбрать параметры печати. При `DoModal` возврате можно определить, выбрал ли пользователь кнопку ОК, применить или Отмена.

Если пользователь нажал кнопку ОК, можно использовать `CPrintDialogEx` функции члена, чтобы получить данные, введенные пользователем.

`CPrintDialogEx::GetDefaults`Функция-член полезна для получения текущих значений по умолчанию для принтера без отображения диалогового окна. Этот метод не требует вмешательства пользователя.

С помощью функции Windows можно `CommDlgExtendedError` определить, произошла ли ошибка во время инициализации диалогового окна, и получить дополнительные сведения об ошибке. Дополнительные сведения об этой функции см. в Windows SDK.

Дополнительные сведения об использовании см `CPrintDialogEx` . в разделе [Общие классы диалоговых окон](../../mfc/common-dialog-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

`IObjectWithSite`

`IPrintDialogCallback`

[CCommonDialog](../../mfc/reference/ccommondialog-class.md)

`CPrintDialogEx`

## <a name="requirements"></a>Требования

**Заголовок:** афксдлгс. h

## <a name="cprintdialogexcprintdialogex"></a><a name="cprintdialogex"></a> Кпринтдиаложекс:: Кпринтдиаложекс

Создание страницы свойств печати Windows.

```
CPrintDialogEx(
    DWORD dwFlags = PD_ALLPAGES | PD_USEDEVMODECOPIES | PD_NOPAGENUMS       | PD_HIDEPRINTTOFILE | PD_NOSELECTION | PD_NOCURRENTPAGE,
    CWnd* pParentWnd = NULL);
```

### <a name="parameters"></a>Параметры

*dwFlags*<br/>
Один или несколько флагов, которые можно использовать для настройки параметров диалогового окна в сочетании с помощью побитового оператора или. Например, флаг PD_ALLPAGES устанавливает диапазон печати по умолчанию для всех страниц документа. Дополнительные сведения об этих флагах см. в описании структуры [принтдлжекс](/windows/win32/api/commdlg/ns-commdlg-printdlgexw) в Windows SDK.

*ппарентвнд*<br/>
Указатель на родительский узел или окно-владелец диалогового окна.

### <a name="remarks"></a>Комментарии

Эта функция члена конструирует только объект. Используйте `DoModal` функцию члена для вывода диалогового окна.

## <a name="cprintdialogexcreateprinterdc"></a><a name="createprinterdc"></a> Кпринтдиаложекс:: Креатепринтердк

Создает контекст устройства принтера (DC) из структур [DEVMODE](/windows/win32/api/wingdi/ns-wingdi-devmodea) и [DEVNAMES](/windows/win32/api/commdlg/ns-commdlg-devnames) .

```
HDC CreatePrinterDC();
```

### <a name="return-value"></a>Возвращаемое значение

Обработайте с созданным контекстом печатающего устройства.

### <a name="remarks"></a>Комментарии

Возвращенный контроллер домена также сохраняется в `hDC` члене [m_pdex](#m_pdex).

Предполагается, что контроллер домена является текущим контроллером домена, и все остальные ранее полученные контроллеры домена должны быть удалены. Эта функция может быть вызвана, и полученный контроллер домена будет использоваться без отображения диалогового окна «Печать».

## <a name="cprintdialogexdomodal"></a><a name="domodal"></a> Кпринтдиаложекс::D Омодал

Эта функция вызывается для отображения страницы свойств печати Windows и позволяет пользователю выбирать различные параметры печати, такие как количество копий, диапазон страниц, а также следует ли выполнять сортировку по копиям.

```
virtual INT_PTR DoModal();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение INT_PTR действительно является HRESULT. См. раздел возвращаемые значения в [принтдлжекс](/previous-versions/windows/desktop/legacy/ms646942\(v=vs.85\)) в Windows SDK.

### <a name="remarks"></a>Комментарии

Если требуется инициализировать различные параметры диалогового окна печати путем установки элементов `m_pdex` структуры, следует сделать это перед вызовом метода `DoModal` , но после создания объекта диалогового окна.

После вызова `DoModal` можно вызвать другие функции члена для получения параметров или данных, вводимых пользователем, в диалоговое окно.

Если при вызове используется флаг PD_RETURNDC `DoModal` , то в `hDC` члене [m_pdex](#m_pdex)будет возвращен контроллер домена. Этот контроллер домена должен быть освобожден с помощью вызова [делетедк](/windows/win32/api/wingdi/nf-wingdi-deletedc) вызывающим объектом `CPrintDialogEx` .

## <a name="cprintdialogexgetcopies"></a><a name="getcopies"></a> Кпринтдиаложекс:: выполняет копирование

Вызовите эту функцию после вызова `DoModal` , чтобы получить количество запрошенных копий.

```
int GetCopies() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число запрошенных копий.

## <a name="cprintdialogexgetdefaults"></a><a name="getdefaults"></a> Кпринтдиаложекс:: параметры по умолчанию

Вызывайте эту функцию для получения значений по умолчанию для принтера по умолчанию без отображения диалогового окна.

```
BOOL GetDefaults();
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если выполнено успешно; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Создает контекст устройства принтера (DC) из структур [DEVMODE](/windows/win32/api/wingdi/ns-wingdi-devmodea) и [DEVNAMES](/windows/win32/api/commdlg/ns-commdlg-devnames) .

`GetDefaults` не отображает страницу свойств печать. Вместо этого он задает `hDevNames` члены и `hDevMode` [m_pdex](#m_pdex) для обработки структур [DEVMODE](/windows/win32/api/wingdi/ns-wingdi-devmodea) и [DEVNAMES](/windows/win32/api/commdlg/ns-commdlg-devnames) , инициализированных для принтера системы по умолчанию. Оба `hDevNames` `hDevMode` значения и должны иметь значение null или выдавать `GetDefaults` ошибку.

Если установлен флаг PD_RETURNDC, эта функция не будет возвращать `hDevNames` `hDevMode` вызывающему объекту и (находится в `m_pdex.hDevNames` и `m_pdex.hDevMode` ), но также будет возвращать контроллер домена в `m_pdex.hDC` . Ответственность за удаление контроллера домена принтера и вызов функции Windows [GlobalFree](/windows/win32/api/winbase/nf-winbase-globalfree) для дескрипторов после завершения работы с `CPrintDialogEx` объектом.

## <a name="cprintdialogexgetdevicename"></a><a name="getdevicename"></a> Кпринтдиаложекс:: Жетдевиценаме

Вызовите эту функцию после вызова [DoModal](#domodal) , чтобы получить имя текущего выбранного принтера, или после вызова метода [Default](#getdefaults) , чтобы получить имя принтера по умолчанию.

```
CString GetDeviceName() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имя выбранного в данный момент принтера.

### <a name="remarks"></a>Комментарии

Используйте указатель на `CString` объект, возвращаемый в `GetDeviceName` качестве значения `lpszDeviceName` в вызове [CDC:: креатедк](../../mfc/reference/cdc-class.md#createdc).

## <a name="cprintdialogexgetdevmode"></a><a name="getdevmode"></a> Кпринтдиаложекс::

Вызовите эту функцию после вызова [DoModal](#domodal) или [по умолчанию](#getdefaults) , чтобы получить сведения о печатающем устройстве.

```
LPDEVMODE GetDevMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Структура данных [DEVMODE](/windows/win32/api/wingdi/ns-wingdi-devmodea) , которая содержит сведения об инициализации устройства и среде драйвера печати. Необходимо разблокировать память, занятую этой структурой, с помощью функции Windows [глобалунлокк](/windows/win32/api/winbase/nf-winbase-globalunlock) , которая описана в Windows SDK.

## <a name="cprintdialogexgetdrivername"></a><a name="getdrivername"></a> Кпринтдиаложекс:: GetDriverName

Вызовите эту функцию после вызова [DoModal](#domodal) или [по умолчанию](#getdefaults) , чтобы получить имя драйвера принтера, определенного системой.

```
CString GetDriverName() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение типа, `CString` указывающее имя драйвера, определяемое системой.

### <a name="remarks"></a>Комментарии

Используйте указатель на `CString` объект, возвращаемый в `GetDriverName` качестве значения *лпсздривернаме* в вызове [CDC:: креатедк](../../mfc/reference/cdc-class.md#createdc).

## <a name="cprintdialogexgetportname"></a><a name="getportname"></a> Кпринтдиаложекс:: Жетпортнаме

Вызовите эту функцию после вызова [DoModal](#domodal) или [по умолчанию](#getdefaults) , чтобы получить имя выбранного в данный момент порта принтера.

```
CString GetPortName() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имя выбранного в данный момент порта принтера.

## <a name="cprintdialogexgetprinterdc"></a><a name="getprinterdc"></a> Кпринтдиаложекс:: Жетпринтердк

Возвращает маркер контекста устройства принтера.

```
HDC GetPrinterDC() const;
```

### <a name="return-value"></a>Возвращаемое значение

Маркер контекста устройства принтера.

### <a name="remarks"></a>Комментарии

Чтобы удалить контекст устройства после завершения его использования, необходимо вызвать функцию Windows [делетедк](/windows/win32/api/wingdi/nf-wingdi-deletedc) .

## <a name="cprintdialogexm_pdex"></a><a name="m_pdex"></a> Кпринтдиаложекс:: m_pdex

Структура ПРИНТДЛЖЕКС, члены которой хранят характеристики объекта диалогового окна.

```
PRINTDLGEX m_pdex;
```

### <a name="remarks"></a>Комментарии

После создания `CPrintDialogEx` объекта можно использовать `m_pdex` для установки различных аспектов диалогового окна перед вызовом функции-члена [DoModal](#domodal) . Дополнительные сведения о `m_pdex` структуре см. в разделе [принтдлжекс](/windows/win32/api/commdlg/ns-commdlg-printdlgexw) в Windows SDK.

При `m_pdex` непосредственном изменении элемента данных будет переопределено поведение по умолчанию.

## <a name="cprintdialogexprintall"></a><a name="printall"></a> Кпринтдиаложекс::P Ринталл

Вызовите эту функцию после вызова `DoModal` , чтобы определить, следует ли печатать все страницы в документе.

```
BOOL PrintAll() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если все страницы документа должны быть распечатаны; в противном случае — FALSE.

## <a name="cprintdialogexprintcollate"></a><a name="printcollate"></a> Кпринтдиаложекс::P Ринтколлате

Вызывайте эту функцию после вызова `DoModal` , чтобы определить, должен ли принтер выполнять сортировку всех печатных копий документа.

```
BOOL PrintCollate() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если пользователь устанавливает флажок COLLATE в диалоговом окне; в противном случае — FALSE.

## <a name="cprintdialogexprintcurrentpage"></a><a name="printcurrentpage"></a> Кпринтдиаложекс::P Ринткуррентпаже

Вызовите эту функцию после вызова `DoModal` , чтобы определить, следует ли печатать текущую страницу в документе.

```
BOOL PrintCurrentPage() const;
```

### <a name="return-value"></a>Возвращаемое значение

TRUE, если в диалоговом окне печати выбран параметр **Печать текущей страницы** ; в противном случае — FALSE.

## <a name="cprintdialogexprintrange"></a><a name="printrange"></a> Кпринтдиаложекс::P Ринтранже

Вызывайте эту функцию после вызова `DoModal` , чтобы определить, следует ли печатать в документе только диапазон страниц.

```
BOOL PrintRange() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если требуется напечатать только диапазон страниц документа. в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Указанные диапазоны страниц можно определить из [m_pdex](#m_pdex) (см `nPageRanges` . раздел, `nMaxPageRanges` и `lpPageRanges` в структуре [принтдлжекс](/windows/win32/api/commdlg/ns-commdlg-printdlgexw) в Windows SDK).

## <a name="cprintdialogexprintselection"></a><a name="printselection"></a> Кпринтдиаложекс::P Ринтселектион

Вызывайте эту функцию после вызова `DoModal` , чтобы определить, следует ли печатать только выбранные в данный момент элементы.

```
BOOL PrintSelection() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если должны быть распечатаны только выбранные элементы; в противном случае — FALSE.

## <a name="see-also"></a>См. также раздел

[Класс Ккоммондиалог](../../mfc/reference/ccommondialog-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Структура CPrintInfo](../../mfc/reference/cprintinfo-structure.md)
