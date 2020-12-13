---
description: 'Дополнительные сведения о: Кконтаинедвиндовт Class'
title: Класс Кконтаинедвиндовт
ms.date: 11/04/2016
f1_keywords:
- CContainedWindowT
- ATLWIN/ATL::CContainedWindowT
- ATLWIN/ATL::CContainedWindowT::CContainedWindowT
- ATLWIN/ATL::CContainedWindowT::Create
- ATLWIN/ATL::CContainedWindowT::DefWindowProc
- ATLWIN/ATL::CContainedWindowT::GetCurrentMessage
- ATLWIN/ATL::CContainedWindowT::RegisterWndSuperclass
- ATLWIN/ATL::CContainedWindowT::SubclassWindow
- ATLWIN/ATL::CContainedWindowT::SwitchMessageMap
- ATLWIN/ATL::CContainedWindowT::UnsubclassWindow
- ATLWIN/ATL::CContainedWindowT::WindowProc
- ATLWIN/ATL::CContainedWindowT::m_dwMsgMapID
- ATLWIN/ATL::CContainedWindowT::m_lpszClassName
- ATLWIN/ATL::CContainedWindowT::m_pfnSuperWindowProc
- ATLWIN/ATL::CContainedWindowT::m_pObject
helpviewer_keywords:
- CContainedWindow class
- contained windows
- CContainedWindowT class
ms.assetid: cde0ca36-9347-4068-995a-d294dae57ca9
ms.openlocfilehash: 68135ec6d8dc43623ec2a827bbe075e24eef8d42
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142081"
---
# <a name="ccontainedwindowt-class"></a>Класс Кконтаинедвиндовт

Этот класс реализует окно, содержащееся в другом объекте.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <class TBase = CWindow, class TWinTraits = CControlWinTraits>
class CContainedWindowT : public TBase
```

#### <a name="parameters"></a>Параметры

*тбасе*<br/>
Базовый класс нового класса. Базовым классом по умолчанию является `CWindow` .

*твинтраитс*<br/>
Класс признаков, определяющий стили окна. Значение по умолчанию — `CControlWinTraits`.

> [!NOTE]
> [Кконтаинедвиндов](ccontainedwindowt-class.md) является специализацией `CContainedWindowT` . Если вы хотите изменить базовый класс или признаки, используйте `CContainedWindowT` напрямую.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кконтаинедвиндовт:: Кконтаинедвиндовт](#ccontainedwindowt)|Конструктор. Инициализирует элементы данных, чтобы указать, какая схема сообщений будет обрабатывать сообщения вложенного окна.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кконтаинедвиндовт:: Create](#create)|Создает окно.|
|[Кконтаинедвиндовт::D Ефвиндовпрок](#defwindowproc)|Обеспечивает обработку сообщений по умолчанию.|
|[Кконтаинедвиндовт:: Жеткуррентмессаже](#getcurrentmessage)|Возвращает текущее сообщение.|
|[Кконтаинедвиндовт:: Регистервндсуперкласс](#registerwndsuperclass)|Регистрирует класс окна автономного окна.|
|[Кконтаинедвиндовт:: Субклассвиндов](#subclasswindow)|Подклассировать окно.|
|[Кконтаинедвиндовт:: Свитчмессажемап](#switchmessagemap)|Изменение схемы сообщений, используемой для обработки сообщений вложенного окна.|
|[Кконтаинедвиндовт:: Унсубклассвиндов](#unsubclasswindow)|Восстанавливает ранее подклассное окно.|
|[Кконтаинедвиндовт:: WindowProc](#windowproc)|Статически Обрабатывает сообщения, отправленные в автономное окно.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Кконтаинедвиндовт:: m_dwMsgMapID](#m_dwmsgmapid)|Определяет, какая схема сообщений будет обрабатывать сообщения вложенного окна.|
|[Кконтаинедвиндовт:: m_lpszClassName](#m_lpszclassname)|Указывает имя существующего класса окна, на котором будет основан новый класс Window.|
|[Кконтаинедвиндовт:: m_pfnSuperWindowProc](#m_pfnsuperwindowproc)|Указывает на исходную процедуру окна класса Window.|
|[Кконтаинедвиндовт:: m_pObject](#m_pobject)|Указывает на содержащий объект.|

## <a name="remarks"></a>Комментарии

`CContainedWindowT` реализует окно, содержащееся в другом объекте. `CContainedWindowT`использует схему сообщений в содержащем объекте для направления сообщений соответствующим обработчикам. При конструировании `CContainedWindowT` объекта указывается, какую карту сообщений следует использовать.

`CContainedWindowT` позволяет создать новое окно, добавив в него класс существующего окна. `Create`Метод сначала регистрирует класс окна, основанный на существующем классе, но использует `CContainedWindowT::WindowProc` . `Create` затем создает окно на основе этого нового класса окна. Каждый экземпляр `CContainedWindowT` может являться суперклассом для другого класса окна.

`CContainedWindowT` также поддерживает подклассы окон. `SubclassWindow`Метод присоединяет существующее окно к `CContainedWindowT` объекту и изменяет процедуру окна на `CContainedWindowT::WindowProc` . Каждый экземпляр `CContainedWindowT` может создать подкласс для другого окна.

> [!NOTE]
> Для любого заданного `CContainedWindowT` объекта вызовите либо `Create` или `SubclassWindow` . Не следует вызывать оба метода в одном и том же объекте.

При использовании параметра **Добавить элемент управления на основе** в мастере проектов ATL мастер автоматически добавляет `CContainedWindowT` элемент данных в класс, реализующий элемент управления. В следующем примере показано, как объявляется вложенное окно:

[!code-cpp[NVC_ATL_Windowing#38](../../atl/codesnippet/cpp/ccontainedwindowt-class_1.h)]

[!code-cpp[NVC_ATL_Windowing#39](../../atl/codesnippet/cpp/ccontainedwindowt-class_2.h)]

[!code-cpp[NVC_ATL_Windowing#40](../../atl/codesnippet/cpp/ccontainedwindowt-class_3.h)]

|Дополнительные сведения|См.|
|--------------------------------|---------|
|Создание элементов управления|[Учебник по ATL](../../atl/active-template-library-atl-tutorial.md)|
|Использование Windows в ATL|[Классы окон ATL](../../atl/atl-window-classes.md)|
|Мастер проектов ATL|[Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)|
|Windows|[Windows](/windows/win32/winmsg/windows) и последующие разделы в Windows SDK|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`TBase`

`CContainedWindowT`

## <a name="requirements"></a>Требования

**Заголовок:** atlwin. h

## <a name="ccontainedwindowtccontainedwindowt"></a><a name="ccontainedwindowt"></a> Кконтаинедвиндовт:: Кконтаинедвиндовт

Конструктор инициализирует элементы данных.

```
CContainedWindowT(
    LPTSTR lpszClassName,
    CMessageMap* pObject,
    DWORD dwMsgMapID = 0);

CContainedWindowT(
    CMessageMap* pObject,
    DWORD dwMsgMapID = 0)
    CContainedWindowT();
```

### <a name="parameters"></a>Параметры

*лпсзкласснаме*<br/>
окне Имя существующего класса окна, на котором будет основано автономное окно.

*Объект*<br/>
окне Указатель на содержащий объект, объявляющий схему сообщения. Класс этого объекта должен быть производным от [кмессажемап](../../atl/reference/cmessagemap-class.md).

*двмсгмапид*<br/>
окне Определяет схему сообщений, которая будет обрабатывать сообщения вложенного окна. Значение по умолчанию 0 указывает схему сообщений по умолчанию, объявленную с помощью [BEGIN_MSG_MAP](message-map-macros-atl.md#begin_msg_map). Чтобы использовать альтернативную схему сообщений, объявленную с помощью [ALT_MSG_MAP (мсгмапид)](message-map-macros-atl.md#alt_msg_map), передайте `msgMapID` .

### <a name="remarks"></a>Комментарии

Если вы хотите создать новое окно с помощью [CREATE](#create), необходимо передать имя существующего класса окна для параметра *лпсзкласснаме* . Пример см. в обзоре [кконтаинедвиндов](../../atl/reference/ccontainedwindowt-class.md) .

Существует три конструктора:

- Конструктор с тремя аргументами — это обычно называемый.

- Конструктор с двумя аргументами использует имя класса из `TBase::GetWndClassName` .

- Если вы хотите предоставить аргументы позже, используется конструктор без аргументов. При последующем вызове необходимо указать имя класса окна, объект схемы сообщения и идентификатор схемы сообщения `Create` .

Если создать подкласс для существующего окна с помощью [субклассвиндов](#subclasswindow), значение *лпсзкласснаме* не будет использоваться. Таким образом, для этого параметра можно передать значение NULL.

## <a name="ccontainedwindowtcreate"></a><a name="create"></a> Кконтаинедвиндовт:: Create

Вызывает [регистервндсуперкласс](#registerwndsuperclass) для регистрации класса окна, основанного на существующем классе, но использующего [Кконтаинедвиндовт:: WindowProc](#windowproc).

```
HWND Create(
    HWND hWndParent,
    _U_RECT rect,
    LPCTSTR szWindowName = NULL,
    DWORD dwStyle = 0,
    DWORD dwExStyle = 0,
    _U_MENUorID MenuOrID = 0U,
    LPVOID lpCreateParam = NULL);

HWND Create(
    CMessageMap* pObject,
    DWORD dwMsgMapID,
    HWND hWndParent,
    _U_RECT rect,
    LPCTSTR szWindowName = NULL,
    DWORD dwStyle = 0,
    DWORD dwExStyle = 0,
    _U_MENUorID MenuOrID = 0U,
    LPVOID lpCreateParam = NULL);

HWND Create(
    LPCTSTR lpszClassName,
    CMessageMap* pObject,
    DWORD dwMsgMapID,
    HWND hWndParent,
    _U_RECT rect,
    LPCTSTR szWindowName = NULL,
    DWORD dwStyle = 0,
    DWORD dwExStyle = 0,
    _U_MENUorID MenuOrID = 0U,
    LPVOID lpCreateParam = NULL);
```

### <a name="parameters"></a>Параметры

*лпсзкласснаме*<br/>
окне Имя существующего класса окна, на котором будет основано автономное окно.

*Объект*<br/>
окне Указатель на содержащий объект, объявляющий схему сообщения. Класс этого объекта должен быть производным от [кмессажемап](../../atl/reference/cmessagemap-class.md).

*двмсгмапид*<br/>
окне Определяет схему сообщений, которая будет обрабатывать сообщения вложенного окна. Значение по умолчанию 0 указывает схему сообщений по умолчанию, объявленную с помощью [BEGIN_MSG_MAP](message-map-macros-atl.md#begin_msg_map). Чтобы использовать альтернативную схему сообщений, объявленную с помощью [ALT_MSG_MAP (мсгмапид)](message-map-macros-atl.md#alt_msg_map), передайте `msgMapID` .

*хвндпарент*<br/>
окне Маркер родительского окна или окно владельца.

*rect*<br/>
окне Структура [Rect](/windows/win32/api/windef/ns-windef-rect) , указывающая расположение окна. `RECT`Может передаваться по указателю или по ссылке.

*сзвиндовнаме*<br/>
окне Задает имя окна. Значение по умолчанию — NULL.

*двстиле*<br/>
окне Стиль окна. Значение по умолчанию — WS_CHILD &#124; WS_VISIBLE. Список возможных значений см. в разделе [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindoww) в Windows SDK.

*двексстиле*<br/>
окне Расширенный стиль окна. Значение по умолчанию — 0, означающее отсутствие расширенного стиля. Список возможных значений см. в разделе [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexw) в Windows SDK.

*менуорид*<br/>
окне Для дочернего окна это идентификатор окна. Для окна верхнего уровня — маркер меню для окна. Значение по умолчанию — **0U**.

*лпкреатепарам*<br/>
окне Указатель на данные для создания окна. Полное описание см. в описании последнего параметра для [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexw).

### <a name="return-value"></a>Возвращаемое значение

В случае успеха — маркер для вновь созданного окна; в противном случае значение NULL.

### <a name="remarks"></a>Комментарии

Существующее имя класса окна сохраняется в [m_lpszClassName](#m_lpszclassname). `Create` затем создает окно на основе этого нового класса. Вновь созданное окно будет автоматически присоединено к `CContainedWindowT` объекту.

> [!NOTE]
> Не вызывайте `Create` , если вы уже вызвали [субклассвиндов](#subclasswindow).

> [!NOTE]
> Если значение 0 используется в качестве значения параметра *менуорид* , его необходимо указать как 0U (значение по умолчанию), чтобы избежать ошибки компилятора.

## <a name="ccontainedwindowtdefwindowproc"></a><a name="defwindowproc"></a> Кконтаинедвиндовт::D Ефвиндовпрок

Вызывается методом [WindowProc](#windowproc) для обработки сообщений, не обрабатываемых схемой сообщений.

```
LRESULT DefWindowProc()
LRESULT DefWindowProc(
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam);
```

### <a name="parameters"></a>Параметры

*Uiacp*<br/>
окне Сообщение, отправленное в окно.

*wParam*<br/>
окне Дополнительные сведения, относящиеся к конкретному сообщению.

*lParam*<br/>
окне Дополнительные сведения, относящиеся к конкретному сообщению.

### <a name="return-value"></a>Возвращаемое значение

Результат обработки сообщения.

### <a name="remarks"></a>Комментарии

По умолчанию `DefWindowProc` вызывает функцию Win32 [каллвиндовпрок](/windows/win32/api/winuser/nf-winuser-callwindowprocw) для отправки сведений о сообщении в процедуру окна, указанную в [m_pfnSuperWindowProc](#m_pfnsuperwindowproc).

## <a name="ccontainedwindowtgetcurrentmessage"></a><a name="getcurrentmessage"></a> Кконтаинедвиндовт:: Жеткуррентмессаже

Возвращает текущее сообщение ( `m_pCurrentMsg` ).

```
const _ATL_MSG* GetCurrentMessage();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее сообщение, упакованное в `MSG` структуру.

## <a name="ccontainedwindowtm_dwmsgmapid"></a><a name="m_dwmsgmapid"></a> Кконтаинедвиндовт:: m_dwMsgMapID

Содержит идентификатор схемы сообщений, используемой в данный момент для автономного окна.

```
DWORD m_dwMsgMapID;
```

### <a name="remarks"></a>Комментарии

Эта схема сообщений должна быть объявлена в содержащем объекте.

Схема сообщений по умолчанию, объявленная с [BEGIN_MSG_MAP](message-map-macros-atl.md#begin_msg_map), всегда идентифицируется нулем. Альтернативная схема сообщений, объявленная с помощью [ALT_MSG_MAP (мсгмапид)](message-map-macros-atl.md#alt_msg_map), определяется `msgMapID` .

`m_dwMsgMapID` Сначала инициализируется конструктором и может быть изменен вызовом [свитчмессажемап](#switchmessagemap). Пример см. в [обзоре кконтаинедвиндовт](../../atl/reference/ccontainedwindowt-class.md).

## <a name="ccontainedwindowtm_lpszclassname"></a><a name="m_lpszclassname"></a> Кконтаинедвиндовт:: m_lpszClassName

Указывает имя существующего класса окна.

```
LPTSTR m_lpszClassName;
```

### <a name="remarks"></a>Комментарии

При создании окна функция [CREATE](#create) регистрирует новый класс Window, основанный на этом существующем классе, но использует [Кконтаинедвиндовт:: WindowProc](#windowproc).

`m_lpszClassName` инициализируется конструктором. Пример см. в обзоре [кконтаинедвиндовт](../../atl/reference/ccontainedwindowt-class.md) .

## <a name="ccontainedwindowtm_pfnsuperwindowproc"></a><a name="m_pfnsuperwindowproc"></a> Кконтаинедвиндовт:: m_pfnSuperWindowProc

Если вложенное окно является подклассом, `m_pfnSuperWindowProc` указывает на исходную процедуру окна класса Window.

```
WNDPROC m_pfnSuperWindowProc;
```

### <a name="remarks"></a>Комментарии

Если в автономном окне используется класс, то есть он основан на классе окна, изменяющем существующий класс, `m_pfnSuperWindowProc` указывает на процедуру окна существующего класса окна.

Метод [дефвиндовпрок](#defwindowproc) отправляет сведения о сообщении в процедуру окна, сохраненную в `m_pfnSuperWindowProc` .

## <a name="ccontainedwindowtm_pobject"></a><a name="m_pobject"></a> Кконтаинедвиндовт:: m_pObject

Указывает на объект, содержащий `CContainedWindowT` объект.

```
CMessageMap* m_pObject;
```

### <a name="remarks"></a>Комментарии

Этот контейнер, класс которого должен быть производным от [кмессажемап](../../atl/reference/cmessagemap-class.md), объявляет схему сообщений, используемую содержащимся в нем окном.

`m_pObject` инициализируется конструктором. Пример см. в обзоре [кконтаинедвиндовт](../../atl/reference/ccontainedwindowt-class.md) .

## <a name="ccontainedwindowtregisterwndsuperclass"></a><a name="registerwndsuperclass"></a> Кконтаинедвиндовт:: Регистервндсуперкласс

Вызывается методом [CREATE](#create) для регистрации класса окна автономного окна.

```
ATOM RegisterWndSuperClass();
```

### <a name="return-value"></a>Возвращаемое значение

В случае успеха атом, однозначно определяющий регистрируемый класс окна; в противном случае — нуль.

### <a name="remarks"></a>Комментарии

Этот класс Window основан на существующем классе, но использует [кконтаинедвиндовт:: WindowProc](#windowproc). Имя и процедура окна существующего класса Window сохраняются в [m_lpszClassName](#m_lpszclassname) и [m_pfnSuperWindowProc](#m_pfnsuperwindowproc)соответственно.

## <a name="ccontainedwindowtsubclasswindow"></a><a name="subclasswindow"></a> Кконтаинедвиндовт:: Субклассвиндов

Подклассировать окно, идентифицируемое *HWND* , и присоединить его к `CContainedWindowT` объекту.

```
BOOL SubclassWindow(HWND hWnd);
```

### <a name="parameters"></a>Параметры

*hWnd*<br/>
окне Маркер окна, для которого создается подкласс.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если окно успешно подклассировать; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

В окне с подклассами теперь используется [кконтаинедвиндовт:: WindowProc](#windowproc). Исходная процедура окна сохраняется в [m_pfnSuperWindowProc](#m_pfnsuperwindowproc).

> [!NOTE]
> Не вызывайте `SubclassWindow` , если вы уже вызвали [CREATE](#create).

## <a name="ccontainedwindowtswitchmessagemap"></a><a name="switchmessagemap"></a> Кконтаинедвиндовт:: Свитчмессажемап

Изменение схемы сообщений, которая будет использоваться для обработки сообщений вложенного окна.

```cpp
void SwitchMessageMap(DWORD dwMsgMapID);
```

### <a name="parameters"></a>Параметры

*двмсгмапид*<br/>
окне Идентификатор схемы сообщения. Чтобы использовать схему сообщений по умолчанию, объявленную с [BEGIN_MSG_MAP](message-map-macros-atl.md#begin_msg_map), передайте нуль. Чтобы использовать альтернативную схему сообщений, объявленную с помощью [ALT_MSG_MAP (мсгмапид)](message-map-macros-atl.md#alt_msg_map), передайте `msgMapID` .

### <a name="remarks"></a>Комментарии

Схема сообщений должна быть определена в содержащем объекте.

В конструкторе изначально указывается идентификатор схемы сообщения.

## <a name="ccontainedwindowtunsubclasswindow"></a><a name="unsubclasswindow"></a> Кконтаинедвиндовт:: Унсубклассвиндов

Отсоединяет окно с подклассом от `CContainedWindowT` объекта и восстанавливает исходную процедуру окна, сохраненную в [m_pfnSuperWindowProc](#m_pfnsuperwindowproc).

```
HWND UnsubclassWindow(BOOL bForce = FALSE);
```

### <a name="parameters"></a>Параметры

*бфорце*<br/>
окне Задайте значение TRUE, чтобы принудительно восстановить исходную процедуру окна, даже если процедура окна для этого `CContainedWindowT` объекта в данный момент не активна. Если *бфорце* имеет значение false и процедура окна для этого `CContainedWindowT` объекта в данный момент не активна, то исходная процедура окна не будет восстановлена.

### <a name="return-value"></a>Возвращаемое значение

Обработчик для ранее подклассов окна. Если *бфорце* имеет значение false и процедура окна для этого `CContainedWindowT` объекта в данный момент не активна, возвращает значение null.

### <a name="remarks"></a>Комментарии

Используйте этот метод только в том случае, если требуется восстановить исходную процедуру окна перед уничтожением окна. В противном случае [WindowProc](#windowproc) автоматически сделает это при уничтожении окна.

## <a name="ccontainedwindowtwindowproc"></a><a name="windowproc"></a> Кконтаинедвиндовт:: WindowProc

Этот статический метод реализует процедуру окна.

```
static LRESULT CALLBACK WindowProc(
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam);
```

### <a name="parameters"></a>Параметры

*hWnd*<br/>
окне Маркер окна.

*Uiacp*<br/>
окне Сообщение, отправленное в окно.

*wParam*<br/>
окне Дополнительные сведения, относящиеся к конкретному сообщению.

*lParam*<br/>
окне Дополнительные сведения, относящиеся к конкретному сообщению.

### <a name="return-value"></a>Возвращаемое значение

Результат обработки сообщения.

### <a name="remarks"></a>Комментарии

`WindowProc` направляет сообщения в схему сообщений, определяемую [m_dwMsgMapID](#m_dwmsgmapid). При необходимости `WindowProc` вызывает [дефвиндовпрок](#defwindowproc) для дополнительной обработки сообщений.

## <a name="see-also"></a>См. также раздел

[Класс CWindow](../../atl/reference/cwindow-class.md)<br/>
[Класс Квиндовимпл](../../atl/reference/cwindowimpl-class.md)<br/>
[Класс Кмессажемап](../../atl/reference/cmessagemap-class.md)<br/>
[BEGIN_MSG_MAP](message-map-macros-atl.md#begin_msg_map)<br/>
[ALT_MSG_MAP (Мсгмапид)](message-map-macros-atl.md#alt_msg_map)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
