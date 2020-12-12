---
description: 'Дополнительные сведения о: Кснапинитемимпл Class'
title: Класс Кснапинитемимпл
ms.date: 11/04/2016
f1_keywords:
- CSnapInItemImpl
- ATLSNAP/ATL::CSnapInItemImpl
- ATLSNAP/ATL::CSnapInItemImpl::CSnapInItemImpl
- ATLSNAP/ATL::CSnapInItemImpl::AddMenuItems
- ATLSNAP/ATL::CSnapInItemImpl::Command
- ATLSNAP/ATL::CSnapInItemImpl::CreatePropertyPages
- ATLSNAP/ATL::CSnapInItemImpl::FillData
- ATLSNAP/ATL::CSnapInItemImpl::GetResultPaneInfo
- ATLSNAP/ATL::CSnapInItemImpl::GetResultViewType
- ATLSNAP/ATL::CSnapInItemImpl::GetScopePaneInfo
- ATLSNAP/ATL::CSnapInItemImpl::Notify
- ATLSNAP/ATL::CSnapInItemImpl::QueryPagesFor
- ATLSNAP/ATL::CSnapInItemImpl::SetMenuInsertionFlags
- ATLSNAP/ATL::CSnapInItemImpl::SetToolbarButtonInfo
- ATLSNAP/ATL::CSnapInItemImpl::UpdateMenuState
- ATLSNAP/ATL::CSnapInItemImpl::UpdateToolbarButton
- ATLSNAP/ATL::CSnapInItemImpl::m_bstrDisplayName
- ATLSNAP/ATL::CSnapInItemImpl::m_resultDataItem
- ATLSNAP/ATL::CSnapInItemImpl::m_scopeDataItem
helpviewer_keywords:
- snap-ins, data items
- snap-ins, ATL support for
- CSnapInItemImpl class
- snap-ins
ms.assetid: 52caefbd-9eae-49b0-add2-d55524271aa7
ms.openlocfilehash: c1c63f5b60d57743087bffde214d9b8addef5b8b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140560"
---
# <a name="csnapinitemimpl-class"></a>Класс Кснапинитемимпл

Этот класс предоставляет методы для реализации объекта узла оснастки.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <class T, BOOL bIsExtension = FALSE>
class ATL_NO_VTABLE CSnapInItemImpl : public CSnapInItem
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `CSnapInItemImpl` .

*бисекстенсион*<br/>
Значение TRUE, если объект является расширением оснастки; в противном случае — FALSE.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кснапинитемимпл:: Кснапинитемимпл](#csnapinitemimpl)|Конструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кснапинитемимпл:: Аддменуитемс](#addmenuitems)|Добавляет пункты меню в контекстное меню.|
|[Кснапинитемимпл:: Command](#command)|Вызывается консолью при выборе пользовательского элемента меню.|
|[Кснапинитемимпл:: Креатепропертипажес](#createpropertypages)|Добавляет страницы в страницу свойств оснастки.|
|[Кснапинитемимпл:: Филлдата](#filldata)|Копирует сведения об объекте оснастки в указанный поток.|
|[Кснапинитемимпл:: Жетресултпанеинфо](#getresultpaneinfo)|Извлекает `RESULTDATAITEM` структуру оснастки.|
|[Кснапинитемимпл:: Жетресултвиевтипе](#getresultviewtype)|Определяет тип представления, используемого панелью результатов.|
|[Кснапинитемимпл:: Жетскопепанеинфо](#getscopepaneinfo)|Извлекает `SCOPEDATAITEM` структуру оснастки.|
|[Кснапинитемимпл:: notify](#notify)|Вызывается консолью для уведомления оснастки о действиях, выполняемых пользователем.|
|[Кснапинитемимпл:: Куерипажесфор](#querypagesfor)|Вызывается, чтобы определить, поддерживает ли узел оснастки страницы свойств.|
|[Кснапинитемимпл:: Сетменуинсертионфлагс](#setmenuinsertionflags)|Изменяет флаги вставки меню для объекта оснастки.|
|[Кснапинитемимпл:: Сеттулбарбуттонинфо](#settoolbarbuttoninfo)|Задает сведения об указанной кнопке панели инструментов.|
|[Кснапинитемимпл:: Упдатеменустате](#updatemenustate)|Обновляет состояние пункта контекстного меню.|
|[Кснапинитемимпл:: Упдатетулбарбуттон](#updatetoolbarbutton)|Обновляет состояние указанной кнопки панели инструментов.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Кснапинитемимпл:: m_bstrDisplayName](#m_bstrdisplayname)|Имя объекта оснастки.|
|[Кснапинитемимпл:: m_resultDataItem](#m_resultdataitem)|Структура Windows, `RESULTDATAITEM` используемая `CSnapInItemImpl` объектом.|
|[Кснапинитемимпл:: m_scopeDataItem](#m_scopedataitem)|Структура Windows, `SCOPEDATAITEM` используемая `CSnapInItemImpl` объектом.|

## <a name="remarks"></a>Комментарии

`CSnapInItemImpl` предоставляет базовую реализацию объекта узла оснастки, например добавление пунктов меню и панелей инструментов, а также перенаправление команд для узла оснастки в соответствующую функцию обработчика. Эти функции реализуются с помощью нескольких различных интерфейсов и типов карт. Реализация по умолчанию обрабатывает уведомления, отправляемые объекту node, определяя правильный экземпляр производного класса, а затем пересылая сообщение в правильный экземпляр.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CSnapInItem`

`CSnapInItemImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлснап. h

## <a name="csnapinitemimpladdmenuitems"></a><a name="addmenuitems"></a> Кснапинитемимпл:: Аддменуитемс

Этот метод реализует функцию Win32 [иекстендконтекстмену:: аддменуитемс](/windows/win32/api/mmc/nf-mmc-iextendcontextmenu-addmenuitems).

```
AddMenuItems(
    LPCONTEXTMENUCALLBACK piCallback,
    long* pInsertionAllowed,
    DATA_OBJECT_TYPES type);
```

### <a name="parameters"></a>Параметры

*пикаллбакк*<br/>
окне Указатель на объект `IContextMenuCallback` , который может добавлять элементы в контекстное меню.

*пинсертионалловед*<br/>
[вход, выход] Определяет в консоли управления (MMC) определенные точки вставки элементов меню, которые можно использовать. Это может быть сочетание следующих флагов:

- CCM_INSERTIONALLOWED_TOP элементы могут быть вставлены в верхней части контекстного меню.

- CCM_INSERTIONALLOWED_NEW элементы можно вставить в подменю создать новое.

- CCM_INSERTIONALLOWED_TASK элементы могут быть вставлены в подменю задача.

- CCM_INSERTIONALLOWED_VIEW элементы могут быть вставлены в меню Вид панели инструментов или в подменю вид контекстного меню панели результатов.

*type*<br/>
окне Указывает тип объекта. Может иметь одно из следующих значений:

- CCT_SCOPE объект данных для контекста области области.

- CCT_RESULT объект данных для контекста области результатов.

- CCT_SNAPIN_MANAGER объект данных для контекста диспетчера оснастки.

- CCT_UNINITIALIZEDный объект данных имеет недопустимый тип.

## <a name="csnapinitemimplcommand"></a><a name="command"></a> Кснапинитемимпл:: Command

Этот метод реализует функцию Win32 [иекстендконтекстмену:: Command](/windows/win32/api/mmc/nf-mmc-iextendcontextmenu-command).

```
Command(long lCommandID, DATA_OBJECT_TYPES type);
```

### <a name="parameters"></a>Параметры

*лкоммандид*<br/>
окне Указывает идентификатор команды для пункта меню.

*type*<br/>
окне Указывает тип объекта. Может иметь одно из следующих значений:

- CCT_SCOPE объект данных для контекста области области.

- CCT_RESULT объект данных для контекста области результатов.

- CCT_SNAPIN_MANAGER объект данных для контекста диспетчера оснастки.

- CCT_UNINITIALIZEDный объект данных имеет недопустимый тип.

## <a name="csnapinitemimplcreatepropertypages"></a><a name="createpropertypages"></a> Кснапинитемимпл:: Креатепропертипажес

Этот метод реализует функцию Win32 [иекстендпропертишит:: креатепропертипажес](/windows/win32/api/mmc/nn-mmc-iextendpropertysheet2).

```
CreatePropertyPages(
    LPPROPERTYSHEETCALLBACK lpProvider,
    long handle,
    IUnknown* pUnk,
    DATA_OBJECT_TYPES type);
```

### <a name="parameters"></a>Параметры

*лппровидер*<br/>
[in] Указатель на интерфейс `IPropertySheetCallback`.

*справиться*<br/>
окне Указывает маркер, используемый для направления сообщения уведомления MMCN_PROPERTY_CHANGE в соответствующий класс данных.

*pUnk*<br/>
окне Указатель на `IExtendPropertySheet` интерфейс объекта, который содержит сведения о контексте узла.

*type*<br/>
окне Указывает тип объекта. Может иметь одно из следующих значений:

- CCT_SCOPE объект данных для контекста области области.

- CCT_RESULT объект данных для контекста области результатов.

- CCT_SNAPIN_MANAGER объект данных для контекста диспетчера оснастки.

- CCT_UNINITIALIZEDный объект данных имеет недопустимый тип.

## <a name="csnapinitemimplcsnapinitemimpl"></a><a name="csnapinitemimpl"></a> Кснапинитемимпл:: Кснапинитемимпл

Формирует объект `CSnapInItemImpl`.

```
CSnapInItemImpl();
```

## <a name="csnapinitemimplfilldata"></a><a name="filldata"></a> Кснапинитемимпл:: Филлдата

Эта функция вызывается для получения сведений об элементе.

```
FillData(CLIPFORMAT cf, LPSTREAM pStream);
```

### <a name="parameters"></a>Параметры

*CF*<br/>
окне Формат (текст, форматированный текст или форматированный текст с элементами OLE) буфера обмена.

*пстреам*<br/>
окне Указатель на поток, содержащий данные объекта.

### <a name="remarks"></a>Комментарии

Чтобы правильно реализовать эту функцию, скопируйте правильные сведения в поток (*пстреам*) в зависимости от формата буфера обмена, указанного в разделе *CF*.

## <a name="csnapinitemimplgetresultviewtype"></a><a name="getresultviewtype"></a> Кснапинитемимпл:: Жетресултвиевтипе

Вызовите эту функцию, чтобы получить тип представления для панели результатов объекта оснастки.

```
GetResultViewType(
    LPOLESTR* ppViewType,
    long* pViewOptions);
```

### <a name="parameters"></a>Параметры

*ппвиевтипе*<br/>
заполняет Указатель на адрес возвращаемого типа представления.

*пвиевоптионс*<br/>
заполняет Указатель на перечисление MMC_VIEW_OPTIONS, которое предоставляет консоль с параметрами, указанными в оснастке "владелец". Значение может быть одним из следующих.

- MMC_VIEW_OPTIONS_NOLISTVIEWS = 0x00000001 указывает консоли отменять представление стандартного представления списка в меню **вид** . Позволяет оснастке отображать собственные пользовательские представления только на панели "представление результатов". Это единственный флаг параметра, определенный в данный момент.

- MMC_VIEW_OPTIONS_NONE = 0 разрешает параметры представления по умолчанию.

## <a name="csnapinitemimplgetscopepaneinfo"></a><a name="getscopepaneinfo"></a> Кснапинитемимпл:: Жетскопепанеинфо

Вызовите эту функцию, чтобы получить `SCOPEDATAITEM` структуру оснастки.

```
GetScopePaneInfo (SCOPEDATAITEM* pScopeDataItem);
```

### <a name="parameters"></a>Параметры

*пскопедатаитем*<br/>
заполняет Указатель на `SCOPEDATAITEM` структуру `CSnapInItemImpl` объекта.

## <a name="csnapinitemimplgetresultpaneinfo"></a><a name="getresultpaneinfo"></a> Кснапинитемимпл:: Жетресултпанеинфо

Вызовите эту функцию, чтобы получить `RESULTDATAITEM` структуру оснастки.

```
GetResultPaneInfo (RESULTDATAITEM* pResultDataItem);
```

### <a name="parameters"></a>Параметры

*пресултдатаитем*<br/>
заполняет Указатель на `RESULTDATAITEM` структуру `CSnapInItemImpl` объекта.

## <a name="csnapinitemimplm_bstrdisplayname"></a><a name="m_bstrdisplayname"></a> Кснапинитемимпл:: m_bstrDisplayName

Содержит строку, отображаемую для элемента узла.

```
CComBSTR m_bstrDisplayName;
```

## <a name="csnapinitemimplm_scopedataitem"></a><a name="m_scopedataitem"></a> Кснапинитемимпл:: m_scopeDataItem

`SCOPEDATAITEM`Структура объекта данных оснастки.

```
SCOPEDATAITEM m_scopeDataItem;
```

## <a name="csnapinitemimplm_resultdataitem"></a><a name="m_resultdataitem"></a> Кснапинитемимпл:: m_resultDataItem

Структура [ресултдатаитем](/windows/win32/api/mmc/ns-mmc-resultdataitem) объекта данных оснастки.

```
RESULTDATAITEM m_resultDataItem;
```

## <a name="csnapinitemimplnotify"></a><a name="notify"></a> Кснапинитемимпл:: notify

Вызывается, когда пользователь работает над объектом оснастки.

```
STDMETHOD(Notify)(
    MMC_NOTIFY_TYPE event,
    long arg,
    long param,
    IComponentData* pComponentData,
    IComponent* pComponent,
    DATA_OBJECT_TYPES type) = 0;
```

### <a name="parameters"></a>Параметры

*event*<br/>
окне Определяет действие, выполняемое пользователем. Возможны следующие уведомления:

- MMCN_ACTIVATE посылается, когда окно активируется и деактивируется.

- MMCN_ADD_IMAGES отправляется на панель результатов для добавления изображений.

- MMCN_BTN_CLICK посылается, когда пользователь нажимает одну из кнопок панели инструментов.

- MMCN_CLICK посылается, когда пользователь нажимает кнопку мыши в элементе представления списка.

- MMCN_DBLCLICK посылается, когда пользователь дважды нажимает кнопку мыши в элементе представления списка.

- MMCN_DELETE отправлена для информирования оснастки о том, что объект должен быть удален.

- MMCN_EXPAND посылается, когда папка нуждается в развертывании или отправке контракта.

- MMCN_MINIMIZED посылается при сворачивании или разворачивании окна.

- MMCN_PROPERTY_CHANGE отправлено для уведомления объекта оснастки о том, что представление объекта оснастки будет изменено.

- MMCN_REMOVE_CHILDREN посылается, когда оснастка должна удалить все поддерево, добавленное ниже указанного узла.

- MMCN_RENAME отправляется в первый раз для запроса переименования, а второй раз — для переименования.

- MMCN_SELECT, отправляемые при выборе элемента в области представления "область" или "результат".

- MMCN_SHOW отправляется при первом выборе или снятии элемента области.

- MMCN_VIEW_CHANGE отправляется, когда оснастка может обновить все представления при возникновении изменений.

*АРГ*<br/>
окне Зависит от типа уведомления.

*param*<br/>
окне Зависит от типа уведомления.

*пкомпонентдата*<br/>
заполняет Указатель на объект, реализующий `IComponentData` . Этот параметр имеет значение NULL, если уведомление не перенаправляется `IComponentData::Notify` .

*пкомпонент*<br/>
заполняет Указатель на объект, реализующий интерфейс `IComponent` . Этот параметр имеет значение NULL, если уведомление не перенаправляется `IComponent::Notify` .

*type*<br/>
окне Указывает тип объекта. Может иметь одно из следующих значений:

- CCT_SCOPE объект данных для контекста области области.

- CCT_RESULT объект данных для контекста области результатов.

- CCT_SNAPIN_MANAGER объект данных для контекста диспетчера оснастки.

- CCT_UNINITIALIZEDный объект данных имеет недопустимый тип.

## <a name="csnapinitemimplquerypagesfor"></a><a name="querypagesfor"></a> Кснапинитемимпл:: Куерипажесфор

Вызывается, чтобы определить, поддерживает ли узел оснастки страницы свойств.

```
QueryPagesFor(DATA_OBJECT_TYPES type);
```

## <a name="csnapinitemimplsetmenuinsertionflags"></a><a name="setmenuinsertionflags"></a> Кснапинитемимпл:: Сетменуинсертионфлагс

Вызовите эту функцию, чтобы изменить флаги вставки меню, заданные параметром *пинсертионалловед*, для объекта оснастки.

```cpp
void SetMenuInsertionFlags(
    bool bBeforeInsertion,
    long* pInsertionAllowed);
```

### <a name="parameters"></a>Параметры

*ббефореинсертион*<br/>
окне Ненулевое значение, если функция должна вызываться до добавления элементов в контекстное меню; в противном случае — 0.

*пинсертионалловед*<br/>
[вход, выход] Определяет в консоли управления (MMC) определенные точки вставки элементов меню, которые можно использовать. Это может быть сочетание следующих флагов:

- CCM_INSERTIONALLOWED_TOP элементы могут быть вставлены в верхней части контекстного меню.

- CCM_INSERTIONALLOWED_NEW элементы можно вставить в подменю создать новое.

- CCM_INSERTIONALLOWED_TASK элементы могут быть вставлены в подменю задача.

- CCM_INSERTIONALLOWED_VIEW элементы могут быть вставлены в меню Вид панели инструментов или в подменю вид контекстного меню панели результатов.

### <a name="remarks"></a>Комментарии

При разработке основной оснастки можно сбросить любой из флагов вставки, чтобы изменить тип элементов меню, которые может добавить расширение стороннего разработчика. Например, основная оснастка может снять флажок CCM_INSERTIONALLOWED_NEW, чтобы расширения не могли добавлять собственные пункты меню создать новые.

Не следует пытаться задать биты в *пинсертионалловед* , которые были изначально удалены. В будущих версиях MMC в настоящее время нельзя использовать BITS, поэтому не следует изменять биты, которые в настоящее время не определены.

## <a name="csnapinitemimplsettoolbarbuttoninfo"></a><a name="settoolbarbuttoninfo"></a> Кснапинитемимпл:: Сеттулбарбуттонинфо

Вызывайте эту функцию, чтобы изменить любые стили кнопок панели инструментов объекта оснастки перед созданием панели инструментов.

```cpp
void SetToolbarButtonInfo(
    UINT id,
    BYTE* fsState,
    BYTE* fsType);
```

### <a name="parameters"></a>Параметры

*id*<br/>
окне Идентификатор заданной кнопки панели инструментов.

*фсстате*<br/>
окне Флаги состояния кнопки. Может быть одним или несколькими из следующих:

- TBSTATE_CHECKED кнопка имеет стиль TBSTYLE_CHECKED и нажата.

- TBSTATE_ENABLED кнопка принимает вводимые пользователем данные. Кнопка, не имеющая этого состояния, не принимает ввод пользователя и является серым.

- TBSTATE_HIDDEN кнопка не отображается и не может принимать данные, вводимые пользователем.

- TBSTATE_INDETERMINATE кнопка неактивна.

- TBSTATE_PRESSED нажатии кнопки.

- TBSTATE_WRAP разрыв строки после кнопки. Кнопка также должна иметь TBSTATE_ENABLED.

*фстипе*<br/>
окне Флаги состояния кнопки. Может быть одним или несколькими из следующих:

- TBSTYLE_BUTTON создает стандартную кнопку отправки.

- TBSTYLE_CHECK создает кнопку, переключающую нажатые и ненажатые состояния каждый раз, когда пользователь щелкает его. Кнопка имеет другой цвет фона, если он находится в нажатом состоянии.

- TBSTYLE_CHECKGROUP создает кнопку проверки, которая остается нажатой, пока не будет нажата другая кнопка в группе.

- TBSTYLE_GROUP создает кнопку, которая остается нажатой, пока не будет нажата другая кнопка в группе.

- TBSTYLE_SEP создает разделитель, предоставляя небольшой зазор между группами кнопок. Кнопка с таким стилем не получает входные данные пользователя.

## <a name="csnapinitemimplupdatemenustate"></a><a name="updatemenustate"></a> Кснапинитемимпл:: Упдатеменустате

Вызывайте эту функцию, чтобы изменить пункт меню перед вставкой в контекстное меню объекта оснастки.

```cpp
void UpdateMenuState(
    UINT id,
    LPTSTR pBuf,
    UINT* flags);
```

### <a name="parameters"></a>Параметры

*id*<br/>
окне ИДЕНТИФИКАТОР устанавливаемого элемента меню.

*пбуф*<br/>
окне Указатель на строку для обновления элемента меню.

*flags*<br/>
окне Задает новые флаги состояния. Это может быть сочетание следующих флагов:

- MF_POPUP Указывает, что это подменю в контекстном меню. Пункты меню, точки вставки и другие вложенные меню можно добавить в это меню, используя его `lCommandID` в качестве `IInsertionPointID` .

- MF_BITMAP и MF_OWNERDRAW эти флаги не разрешены и будут возвращать возвращаемое значение E_INVALIDARG.

- MF_SEPARATOR рисует горизонтальную разделительную линию. `IContextMenuProvider`Разрешено добавлять элементы меню только с набором MF_SEPARATOR.

- MF_CHECKED помещает галочку рядом с пунктом меню.

- MF_DISABLED отключает пункт меню, поэтому он не может быть выбран, но флаг не отображается серым цветом.

- MF_ENABLED позволяет выбрать пункт меню для выбора, восстанавливая его из серого состояния.

- MF_GRAYED отключает пункт меню, выключая его серым, поэтому он не может быть выбран.

- MF_MENUBARBREAK функции аналогичны флагу MF_MENUBREAK для строки меню. Для раскрывающегося меню, подменю или контекстного меню новый столбец отделяется от старого в вертикальной линией.

- MF_MENUBREAK помещает элемент в новую строку (для строки меню) или в новый столбец (для раскрывающегося меню, подменю или контекстного меню) без разделения столбцов.

- MF_UNCHECKED не установлен флажок рядом с элементом (по умолчанию).

Следующие группы флагов нельзя использовать совместно:

- MF_DISABLED, MF_ENABLED и MF_GRAYED.

- MF_MENUBARBREAK и MF_MENUBREAK.

- MF_CHECKED и MF_UNCHECKED.

## <a name="csnapinitemimplupdatetoolbarbutton"></a><a name="updatetoolbarbutton"></a> Кснапинитемимпл:: Упдатетулбарбуттон

Вызывайте эту функцию, чтобы изменить кнопку на панели инструментов объекта оснастки перед отображением.

```
BOOL UpdateToolbarButton(UINT id, BYTE fsState);
```

### <a name="parameters"></a>Параметры

*id*<br/>
Указывает идентификатор кнопки для обновления кнопки панели инструментов.

*фсстате*<br/>
Задает состояние кнопки панели инструментов. Если это состояние задано, возвращается значение TRUE. Это может быть сочетание следующих флагов:

- Включение кнопки принимает вводимые пользователем данные. Кнопка, не имеющая этого состояния, не принимает ввод пользователя и является серым.

- УСТАНОВЛЕН флажок установленный стиль и нажата кнопка.

- СКРЫТая кнопка не видна и не может принимать данные, вводимые пользователем.

- Неопределенное значение кнопки является серым.

- БУТТОНПРЕССЕД нажатии кнопки.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
