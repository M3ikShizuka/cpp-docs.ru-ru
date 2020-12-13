---
description: 'Дополнительные сведения о: Кмаусеманажер Class'
title: Класс Кмаусеманажер
ms.date: 11/04/2016
f1_keywords:
- CMouseManager
- AFXMOUSEMANAGER/CMouseManager
- AFXMOUSEMANAGER/CMouseManager::AddView
- AFXMOUSEMANAGER/CMouseManager::GetViewDblClickCommand
- AFXMOUSEMANAGER/CMouseManager::GetViewIconId
- AFXMOUSEMANAGER/CMouseManager::GetViewIdByName
- AFXMOUSEMANAGER/CMouseManager::GetViewNames
- AFXMOUSEMANAGER/CMouseManager::LoadState
- AFXMOUSEMANAGER/CMouseManager::SaveState
- AFXMOUSEMANAGER/CMouseManager::SetCommandForDblClk
helpviewer_keywords:
- CMouseManager [MFC], AddView
- CMouseManager [MFC], GetViewDblClickCommand
- CMouseManager [MFC], GetViewIconId
- CMouseManager [MFC], GetViewIdByName
- CMouseManager [MFC], GetViewNames
- CMouseManager [MFC], LoadState
- CMouseManager [MFC], SaveState
- CMouseManager [MFC], SetCommandForDblClk
ms.assetid: a4d05017-4e44-4a40-8b57-4ece0de20481
ms.openlocfilehash: 9816583aa9d05b76f97f1be1487898b5827fbcae
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331562"
---
# <a name="cmousemanager-class"></a>Класс Кмаусеманажер

Позволяет пользователю связать различные команды с определенным объектом [CView](../../mfc/reference/cview-class.md) , когда пользователь дважды щелкнет внутри этого представления.

## <a name="syntax"></a>Синтаксис

```
class CMouseManager : public CObject
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмаусеманажер:: Аддвиев](#addview)|Добавляет `CView` объект в диалоговое окно **настройки** . Диалоговое окно **Настройка** позволяет пользователю связать двойной щелчок с командой для каждого из перечисленных представлений.|
|[Кмаусеманажер:: Жетвиевдблкликккомманд](#getviewdblclickcommand)|Возвращает команду, которая выполняется, когда пользователь дважды щелкает в указанном представлении.|
|[Кмаусеманажер:: Жетвиевиконид](#getviewiconid)|Возвращает значок, связанный с указанным ИДЕНТИФИКАТОРом представления.|
|[Кмаусеманажер:: Жетвиевидбинаме](#getviewidbyname)|Возвращает идентификатор представления, связанный с указанным именем представления.|
|[Кмаусеманажер:: Жетвиевнамес](#getviewnames)|Извлекает список всех добавленных имен представлений.|
|[Кмаусеманажер:: LoadState](#loadstate)|Загружает `CMouseManager` состояние из реестра Windows.|
|[Кмаусеманажер:: SaveState](#savestate)|Записывает `CMouseManager` состояние в реестр Windows.|
|[Кмаусеманажер:: Сеткоммандфордблклк](#setcommandfordblclk)|Связывает указанную команду и предоставленное представление.|

## <a name="remarks"></a>Комментарии

`CMouseManager`Класс поддерживает коллекцию `CView` объектов. Каждое представление идентифицируется по имени и ИДЕНТИФИКАТОРу. Эти представления отображаются в диалоговом окне **Настройка** . Пользователь может изменить команду, связанную с любым представлением, в диалоговом окне **Настройка** . Связанная команда выполняется, когда пользователь дважды щелкает в этом представлении. Для поддержки этой функции с точки зрения кода необходимо обработать сообщение WM_LBUTTONDBLCLK и вызвать функцию [CWinAppEx:: онвиевдаублекликк](../../mfc/reference/cwinappex-class.md#onviewdoubleclick) в коде для этого `CView` объекта.

Не следует создавать `CMouseManager` объект вручную. Он будет создан платформой приложения. Он также будет удален автоматически при выходе пользователя из приложения. Чтобы получить указатель на диспетчер мыши для своего приложения, вызовите [CWinAppEx:: жетмаусеманажер](../../mfc/reference/cwinappex-class.md#getmousemanager).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CMouseManager`

## <a name="requirements"></a>Требования

**Заголовок:** афксмаусеманажер. h

## <a name="cmousemanageraddview"></a><a name="addview"></a> Кмаусеманажер:: Аддвиев

Регистрирует объект [CView](../../mfc/reference/cview-class.md) с [классом кмаусеманажер](../../mfc/reference/cmousemanager-class.md) для поддержки пользовательского поведения мыши.

```
BOOL AddView(
    int iViewId,
    UINT uiViewNameResId,
    UINT uiIconId = 0);

BOOL AddView(
    int iId,
    LPCTSTR lpszViewName,
    UINT uiIconId = 0);
```

### <a name="parameters"></a>Параметры

*ивиевид*<br/>
окне Идентификатор представления.

*уивиевнамересид*<br/>
окне Идентификатор строки ресурса, ссылающийся на имя представления.

*уииконид*<br/>
окне ИДЕНТИФИКАТОР значка представления.

*iId*<br/>
окне Идентификатор представления.

*лпсзвиевнаме*<br/>
окне Имя представления.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Для поддержки пользовательского поведения мыши представление должно быть зарегистрировано в `CMouseManager` объекте. Любой объект, производный от `CView` класса, может быть зарегистрирован в диспетчере мыши. Строка и значок, связанные с представлением, отображаются на вкладке **мышь** диалогового окна **Настройка** .

Разработчик обязан создавать и поддерживать идентификаторы представлений, такие как *ивиевид* и *IID*.

Дополнительные сведения о том, как обеспечить пользовательское поведение мыши, см. в разделе [Настройка клавиатуры и мыши](../../mfc/keyboard-and-mouse-customization.md).

### <a name="example"></a>Пример

В следующем примере показано, как получить указатель на объект с `CMouseManager` помощью `CWinAppEx::GetMouseManager` метода и `AddView` метода в `CMouseManager` классе. Этот фрагмент кода является частью [примера сбора](../../overview/visual-cpp-samples.md)данных о состоянии.

[!code-cpp[NVC_MFC_StateCollection#4](../../mfc/reference/codesnippet/cpp/cmousemanager-class_1.cpp)]

## <a name="cmousemanagergetviewdblclickcommand"></a><a name="getviewdblclickcommand"></a> Кмаусеманажер:: Жетвиевдблкликккомманд

Возвращает команду, которая выполняется, когда пользователь дважды щелкает в указанном представлении.

```
UINT GetViewDblClickCommand(int iId) const;
```

### <a name="parameters"></a>Параметры

*iId*<br/>
окне Идентификатор представления.

### <a name="return-value"></a>Возвращаемое значение

Идентификатор команды, если представление связано с командой; в противном случае — 0.

## <a name="cmousemanagergetviewiconid"></a><a name="getviewiconid"></a> Кмаусеманажер:: Жетвиевиконид

Извлекает значок, связанный с ИДЕНТИФИКАТОРом представления.

```
UINT GetViewIconId(int iViewId) const;
```

### <a name="parameters"></a>Параметры

*ивиевид*<br/>
окне Идентификатор представления.

### <a name="return-value"></a>Возвращаемое значение

Идентификатор ресурса значка в случае успешного выполнения; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Этот метод завершится ошибкой, если представление не было сначала зарегистрировано с помощью [кмаусеманажер:: аддвиев](#addview).

## <a name="cmousemanagergetviewidbyname"></a><a name="getviewidbyname"></a> Кмаусеманажер:: Жетвиевидбинаме

Возвращает идентификатор представления, связанный с именем представления.

```
int GetViewIdByName(LPCTSTR lpszName) const;
```

### <a name="parameters"></a>Параметры

*лпсзнаме*<br/>
окне Имя представления.

### <a name="return-value"></a>Возвращаемое значение

Идентификатор представления в случае успеха; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Этот метод выполняет поиск в представлениях, зарегистрированных с помощью [кмаусеманажер:: аддвиев](#addview).

## <a name="cmousemanagergetviewnames"></a><a name="getviewnames"></a> Кмаусеманажер:: Жетвиевнамес

Извлекает список всех зарегистрированных имен представлений.

```cpp
void GetViewNames(CStringList& listOfNames) const;
```

### <a name="parameters"></a>Параметры

*листофнамес*<br/>
заполняет Ссылка на `CStringList` объект.

### <a name="remarks"></a>Комментарии

Этот метод заполняет параметр `listOfNames` именами всех представлений, зарегистрированных с помощью [кмаусеманажер:: аддвиев](#addview).

## <a name="cmousemanagerloadstate"></a><a name="loadstate"></a> Кмаусеманажер:: LoadState

Загружает состояние [класса кмаусеманажер](../../mfc/reference/cmousemanager-class.md) из реестра.

```
BOOL LoadState(LPCTSTR lpszProfileName = NULL);
```

### <a name="parameters"></a>Параметры

*лпсзпрофиленаме*<br/>
окне Путь к разделу реестра.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Сведения о состоянии, загруженные из реестра, включают в себя зарегистрированные представления, идентификаторы представлений и связанные команды. Если параметр *лпсзпрофиленаме* имеет значение null, эта функция загружает `CMouseManager` данные из расположения реестра по умолчанию, управляемого [классом CWinAppEx](../../mfc/reference/cwinappex-class.md).

В большинстве случаев нет необходимости вызывать эту функцию напрямую. Он вызывается как часть процесса инициализации рабочей области. Дополнительные сведения о процессе инициализации рабочей области см. в разделе [CWinAppEx:: LoadState](../../mfc/reference/cwinappex-class.md#loadstate).

## <a name="cmousemanagersavestate"></a><a name="savestate"></a> Кмаусеманажер:: SaveState

Записывает состояние [класса кмаусеманажер](../../mfc/reference/cmousemanager-class.md) в реестр.

```
BOOL SaveState(LPCTSTR lpszProfileName = NULL);
```

### <a name="parameters"></a>Параметры

*лпсзпрофиленаме*<br/>
окне Путь к разделу реестра.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Сведения о состоянии, записанные в реестр, включают все зарегистрированные представления, идентификаторы представлений и связанные команды. Если параметр *лпсзпрофиленаме* имеет значение null, эта функция записывает `CMouseManager` данные в расположение реестра по умолчанию, управляемое [классом CWinAppEx](../../mfc/reference/cwinappex-class.md).

В большинстве случаев нет необходимости вызывать эту функцию напрямую. Он вызывается как часть процесса сериализации рабочей области. Дополнительные сведения о процессе сериализации рабочей области см. в разделе [CWinAppEx:: SaveState](../../mfc/reference/cwinappex-class.md#savestate).

## <a name="cmousemanagersetcommandfordblclk"></a><a name="setcommandfordblclk"></a> Кмаусеманажер:: Сеткоммандфордблклк

Связывает пользовательскую команду с представлением, которое впервые зарегистрировано в диспетчере мыши.

```cpp
void SetCommandForDblClk(
    int iViewId,
    UINT uiCmd);
```

### <a name="parameters"></a>Параметры

*ивиевид*<br/>
окне Идентификатор представления.

*уикмд*<br/>
[in] Идентификатор команды.

### <a name="remarks"></a>Комментарии

Чтобы связать пользовательскую команду с представлением, необходимо сначала зарегистрировать представление с помощью [кмаусеманажер:: аддвиев](#addview). Для `AddView` метода требуется идентификатор представления в качестве входного параметра. После регистрации представления можно вызвать `CMouseManager::SetCommandForDblClk` с тем же входным параметром идентификатора представления, который вы указали в `AddView` . Затем, когда пользователь дважды щелкает мышью в зарегистрированном представлении, приложение выполнит команду, указанную параметром *уикмд.* Для поддержки пользовательского поведения мыши также потребуется настроить представление, зарегистрированное в диспетчере мыши. Дополнительные сведения о пользовательском поведении мыши см. в разделе [Настройка клавиатуры и мыши](../keyboard-and-mouse-customization.md).

Если *уикмд* имеет значение 0, указанное представление больше не связано с командой.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CWinAppEx](../../mfc/reference/cwinappex-class.md)<br/>
[Настройка клавиатуры и мыши](../../mfc/keyboard-and-mouse-customization.md)
