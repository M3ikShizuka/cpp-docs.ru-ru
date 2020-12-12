---
description: 'Дополнительные сведения о: Кжумплист Class'
title: Класс Кжумплист
ms.date: 03/27/2019
f1_keywords:
- CJumpList
- AFXADV/CJumpList
- AFXADV/CJumpList::CJumpList
- AFXADV/CJumpList::AbortList
- AFXADV/CJumpList::AddDestination
- AFXADV/CJumpList::AddKnownCategory
- AFXADV/CJumpList::AddTask
- AFXADV/CJumpList::AddTasks
- AFXADV/CJumpList::AddTaskSeparator
- AFXADV/CJumpList::ClearAll
- AFXADV/CJumpList::ClearAllDestinations
- AFXADV/CJumpList::CommitList
- AFXADV/CJumpList::GetDestinationList
- AFXADV/CJumpList::GetMaxSlots
- AFXADV/CJumpList::GetRemovedItems
- AFXADV/CJumpList::InitializeList
- AFXADV/CJumpList::SetAppID
helpviewer_keywords:
- CJumpList [MFC], CJumpList
- CJumpList [MFC], AbortList
- CJumpList [MFC], AddDestination
- CJumpList [MFC], AddKnownCategory
- CJumpList [MFC], AddTask
- CJumpList [MFC], AddTasks
- CJumpList [MFC], AddTaskSeparator
- CJumpList [MFC], ClearAll
- CJumpList [MFC], ClearAllDestinations
- CJumpList [MFC], CommitList
- CJumpList [MFC], GetDestinationList
- CJumpList [MFC], GetMaxSlots
- CJumpList [MFC], GetRemovedItems
- CJumpList [MFC], InitializeList
- CJumpList [MFC], SetAppID
ms.assetid: d364d27e-f512-4b12-9872-c2a17c78ab1f
ms.openlocfilehash: 07e896c5b3a205a44850d45dcc4876103a48f2fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97236910"
---
# <a name="cjumplist-class"></a>Класс Кжумплист

А `CJumpList` — это список ярлыков, отображаемых при щелчке значка правой кнопкой мыши на панели задач.

## <a name="syntax"></a>Синтаксис

```
class CJumpList;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кжумплист:: Кжумплист](#cjumplist)|Формирует объект `CJumpList`.|
|[Кжумплист:: ~ Кжумплист](#_dtorcjumplist)|Уничтожает объект `CJumpList` .|

|Имя|Описание|
|----------|-----------------|
|[Кжумплист:: Абортлист](#abortlist)|Прерывает транзакцию создания списка без фиксации.|
|[Кжумплист:: Адддестинатион](#adddestination)|Перегружен. Добавляет назначение в список.|
|[Кжумплист:: Аддкновнкатегори](#addknowncategory)|Добавляет к списку известную категорию.|
|[Кжумплист:: AddTask](#addtask)|Перегружен. Добавляет элементы в категорию канонических задач.|
|[Кжумплист:: Аддтаскс](#addtasks)|Добавляет элементы в категорию канонических задач.|
|[Кжумплист:: Аддтасксепаратор](#addtaskseparator)|Добавляет разделитель между задачами.|
|[Кжумплист:: ClearAll](#clearall)|Удаляет все задачи и назначения, добавленные в текущий экземпляр до `CJumpList` сих пор.|
|[Кжумплист:: Клеараллдестинатионс](#clearalldestinations)|Удаляет все назначения, которые были добавлены к текущему экземпляру `CJumpList` до сих пор.|
|[Кжумплист:: Коммитлист](#commitlist)|Завершает транзакцию сборки списка и фиксирует полученный список в связанном хранилище (в данном случае в реестре).|
|[Кжумплист:: Жетдестинатионлист](#getdestinationlist)|Извлекает указатель интерфейса на список назначения.|
|[Кжумплист:: Жетмаксслотс](#getmaxslots)|Возвращает максимальное количество элементов, включая заголовки категорий, которые могут отображаться в меню назначения вызывающего приложения.|
|[Кжумплист:: Жетремоведитемс](#getremoveditems)|Возвращает массив элементов, представляющих удаленные назначения.|
|[Кжумплист:: Инитиализелист](#initializelist)|Начинает транзакцию сборки списка.|
|[Кжумплист:: Сетаппид](#setappid)|Задает идентификатор модели пользователя приложения для списка, который будет построен.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CJumpList](../../mfc/reference/cjumplist-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксадв. h

## <a name="cjumplistcjumplist"></a><a name="_dtorcjumplist"></a> Кжумплист:: ~ Кжумплист

Уничтожает объект `CJumpList` .

```
~CJumpList();
```

## <a name="cjumplistabortlist"></a><a name="abortlist"></a> Кжумплист:: Абортлист

Прерывает транзакцию создания списка без фиксации.

```cpp
void AbortList();
```

### <a name="remarks"></a>Комментарии

Вызов этого метода оказывает тот же результат, что и удаление `CJumpList` без вызова `CommitList` .

## <a name="cjumplistadddestination"></a><a name="adddestination"></a> Кжумплист:: Адддестинатион

Добавляет назначение в список.

```
BOOL AddDestination(
    LPCTSTR lpcszCategoryName,
    LPCTSTR strDestinationPath);

BOOL AddDestination(
    LPCTSTR strCategoryName,
    IShellItem* pShellItem);

BOOL AddDestination(
    LPCTSTR strCategoryName,
    IShellLink* pShellLink);
```

### <a name="parameters"></a>Параметры

*лпксзкатегоринаме*<br/>
Указывает имя категории. Если указанная категория не существует, она будет создана.

*стрдестинатионпас*<br/>
Указывает путь к целевому файлу.

*стркатегоринаме*<br/>
Указывает имя категории. Если указанная категория не существует, она будет создана.

*пшеллитем*<br/>
Указывает элемент оболочки, представляющий добавляемый объект назначения.

*пшелллинк*<br/>
Указывает ссылку на оболочку, представляющую добавляемый объект назначения.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Экземпляр `CJumpList` внутренне накапливает добавленные назначения и затем фиксирует их в `CommitList` .

## <a name="cjumplistaddknowncategory"></a><a name="addknowncategory"></a> Кжумплист:: Аддкновнкатегори

Добавляет к списку известную категорию.

```
BOOL AddKnownCategory(KNOWNDESTCATEGORY category);
```

### <a name="parameters"></a>Параметры

*category*<br/>
Указывает известный тип категории. Может быть либо KDC_RECENT, либо KDC_KNOWN.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Известные категории — это часто и последние категории, которые будут автоматически вычисляться для каждого приложения, использующего `SHAddToRecentDocs` (или неявно использующего его, так как оболочка вызовет его от имени приложения в некоторых сценариях).

## <a name="cjumplistaddtask"></a><a name="addtask"></a> Кжумплист:: AddTask

Добавляет элементы в категорию канонических задач.

```
BOOL AddTask(
    LPCTSTR strTargetExecutablePath,
    LPCTSTR strCommandLineArgs,
    LPCTSTR strTitle,
    LPCTSTR strIconLocation,
    int iIconIndex);

BOOL AddTask(IShellLink* pShellLink);
```

### <a name="parameters"></a>Параметры

*стртаржетексекутаблепас*<br/>
Указывает путь к целевой задаче.

*стркоммандлинеаргс*<br/>
Задает аргументы командной строки исполняемого файла, заданного параметром *стртаржетексекутаблепас*.

*стртитле*<br/>
Имя задачи, которое будет отображаться в списке назначения.

*стриконлокатион*<br/>
Расположение значка, который будет отображаться в списке назначения вместе с заголовком.

*иикониндекс*<br/>
Индекс значка.

*пшелллинк*<br/>
Ссылка на оболочку, представляющая добавляемую задачу.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Экземпляр `CJumpList` накапливает указанные задачи и добавляет их в список назначения во время `CommitList` . Элементы задач будут отображаться в категории в нижней части меню назначения приложения. Эта категория имеет приоритет над всеми другими категориями, если она заполнена в пользовательском интерфейсе.

## <a name="cjumplistaddtasks"></a><a name="addtasks"></a> Кжумплист:: Аддтаскс

Добавляет элементы в категорию канонических задач.

```
BOOL AddTasks(IObjectArray* pObjectCollection);
```

### <a name="parameters"></a>Параметры

*побжектколлектион*<br/>
Коллекция добавляемых задач.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Экземпляр Кжумплист накапливает указанные задачи и добавляет их в список назначения во время `CommitList` . Элементы задач будут отображаться в категории в нижней части меню назначения приложения. Эта категория имеет приоритет над всеми другими категориями, если она заполнена в пользовательском интерфейсе.

## <a name="cjumplistaddtaskseparator"></a><a name="addtaskseparator"></a> Кжумплист:: Аддтасксепаратор

Добавляет разделитель между задачами.

```
BOOL AddTaskSeparator();
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если оно выполнено успешно, 0 — если нет.

## <a name="cjumplistcjumplist"></a><a name="cjumplist"></a> Кжумплист:: Кжумплист

Формирует объект `CJumpList`.

```
CJumpList(BOOL bAutoCommit = TRUE);
```

### <a name="parameters"></a>Параметры

*баутокоммит*<br/>
Если этот параметр имеет значение FALSE, список не фиксируется автоматически в деструкторе.

## <a name="cjumplistclearall"></a><a name="clearall"></a> Кжумплист:: ClearAll

Удаляет все задачи и назначения, добавленные в текущий экземпляр до `CJumpList` сих пор.

```cpp
void ClearAll();
```

### <a name="remarks"></a>Комментарии

Этот метод очищает и освобождает все данные и внутренние интерфейсы.

## <a name="cjumplistclearalldestinations"></a><a name="clearalldestinations"></a> Кжумплист:: Клеараллдестинатионс

Удаляет все назначения, добавленные в текущий экземпляр Кжумплист на данный момент.

```cpp
void ClearAllDestinations();
```

### <a name="remarks"></a>Комментарии

Вызывайте эту функцию, если необходимо удалить все назначения, добавленные до сих пор в текущем сеансе создания списка назначения, и снова добавить другие назначения. Если внутренняя `ICustomDestinationList` Инициализация выполнена, она остается в активном состоянии.

## <a name="cjumplistcommitlist"></a><a name="commitlist"></a> Кжумплист:: Коммитлист

Завершает транзакцию сборки списка и фиксирует полученный список в связанном хранилище (в данном случае в реестре).

```
BOOL CommitList();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Фиксация является атомарной. При сбое фиксации будет возвращена ошибка.  Когда `CommitList` вызывается, текущий список удаленных элементов будет очищен. Вызов этого метода приводит к сбросу объекта, чтобы он не имел транзакции с активным списком. Чтобы обновить список, необходимо `BeginList` повторно вызвать метод.

## <a name="cjumplistgetdestinationlist"></a><a name="getdestinationlist"></a> Кжумплист:: Жетдестинатионлист

Извлекает указатель интерфейса на список назначения.

```
ICustomDestinationList* GetDestinationList();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Если список переходов не был инициализирован или был зафиксирован или прерван, возвращаемое значение будет равно NULL.

## <a name="cjumplistgetmaxslots"></a><a name="getmaxslots"></a> Кжумплист:: Жетмаксслотс

Возвращает максимальное количество элементов, включая заголовки категорий, которые могут отображаться в меню назначения вызывающего приложения.

```
UINT GetMaxSlots() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Приложения могут сообщать только о количестве элементов и заголовках категорий, Объединенных с этим значением. Если вызывает метод `AppendCategory` , `AppendKnownCategory` или `AddUserTasks` превышает это число, он возвратит ошибку.

## <a name="cjumplistgetremoveditems"></a><a name="getremoveditems"></a> Кжумплист:: Жетремоведитемс

Возвращает массив элементов, представляющих удаленные назначения.

```
IObjectArray* GetRemovedItems();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Удаленные назначения извлекаются во время инициализации списка переходов. При создании нового списка назначения предполагается, что приложения сначала обрабатывали список удаленных назначений, удаляя данные отслеживания для любого элемента, возвращенного перечислителем списка удаленных списков. Если приложение пытается предоставить элемент, который был только что удален в транзакции, которая была запущена текущим вызовом `BeginList` , вызов метода, повторно добавленный в этот элемент, завершится ошибкой, чтобы обеспечить соответствие приложений удаленному списку.

## <a name="cjumplistinitializelist"></a><a name="initializelist"></a> Кжумплист:: Инитиализелист

Начинает транзакцию сборки списка.

```
BOOL InitializeList();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Вам не нужно вызывать этот метод явно, если вы не хотите получить указатель на `ICustomDestinationList` использование `GetDestinationList` , число доступных слотов, использующих `GetMaxSlots` , или список удаленных элементов с помощью `GetRemovedItems` .

## <a name="cjumplistsetappid"></a><a name="setappid"></a> Кжумплист:: Сетаппид

Задает идентификатор модели пользователя приложения для списка, который будет построен.

```cpp
void SetAppID(LPCTSTR strAppID);
```

### <a name="parameters"></a>Параметры

*страппид*<br/>
Строка, указывающая идентификатор модели пользователя приложения.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
