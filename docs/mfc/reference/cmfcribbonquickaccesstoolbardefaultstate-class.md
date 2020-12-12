---
description: 'Дополнительные сведения о: Кмфкриббонкуиккакцесстулбардефаултстате Class'
title: Класс Кмфкриббонкуиккакцесстулбардефаултстате
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonQuickAccessToolBarDefaultState
- AFXRIBBONQUICKACCESSTOOLBAR/CMFCRibbonQuickAccessToolBarDefaultState
- AFXRIBBONQUICKACCESSTOOLBAR/CMFCRibbonQuickAccessToolBarDefaultState::CMFCRibbonQuickAccessToolBarDefaultState
- AFXRIBBONQUICKACCESSTOOLBAR/CMFCRibbonQuickAccessToolBarDefaultState::AddCommand
- AFXRIBBONQUICKACCESSTOOLBAR/CMFCRibbonQuickAccessToolBarDefaultState::CopyFrom
- AFXRIBBONQUICKACCESSTOOLBAR/CMFCRibbonQuickAccessToolBarDefaultState::RemoveAll
helpviewer_keywords:
- CMFCRibbonQuickAccessToolBarDefaultState [MFC], CMFCRibbonQuickAccessToolBarDefaultState
- CMFCRibbonQuickAccessToolBarDefaultState [MFC], AddCommand
- CMFCRibbonQuickAccessToolBarDefaultState [MFC], CopyFrom
- CMFCRibbonQuickAccessToolBarDefaultState [MFC], RemoveAll
ms.assetid: eca99200-b87b-47ba-b2e8-2f3f2444b176
ms.openlocfilehash: d6cd0c32cd8698259de0a78a6a6a7dc42012e92f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321810"
---
# <a name="cmfcribbonquickaccesstoolbardefaultstate-class"></a>Класс Кмфкриббонкуиккакцесстулбардефаултстате

Вспомогательный класс, который управляет состоянием по умолчанию для панели быстрого доступа, расположенной на панели ленты ( [класс CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md)).

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonQuickAccessToolBarDefaultState
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонкуиккакцесстулбардефаултстате:: Кмфкриббонкуиккакцесстулбардефаултстате](#cmfcribbonquickaccesstoolbardefaultstate)|Формирует объект `CMFCRibbonQuickAccessToolbarDefaultState`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонкуиккакцесстулбардефаултстате:: AddCommand](#addcommand)|Добавляет команду в состояние по умолчанию для панели быстрого доступа. Это не приводит к изменению самой панели инструментов.|
|[Кмфкриббонкуиккакцесстулбардефаултстате:: CopyFrom](#copyfrom)|Копирует свойства одной панели быстрого доступа в другую.|
|[Кмфкриббонкуиккакцесстулбардефаултстате:: RemoveAll](#removeall)|Удаляет все команды с панели быстрого доступа. Это не приводит к изменению самой панели инструментов.|

## <a name="remarks"></a>Комментарии

После создания панели быстрого доступа в приложении рекомендуется установить его состояние по умолчанию, вызвав [CMFCRibbonBar:: сеткуиккакцессдефаултстате](../../mfc/reference/cmfcribbonbar-class.md#setquickaccessdefaultstate). Это состояние по умолчанию восстанавливается, когда пользователь нажимает кнопку **Сброс** на странице **Настройка** диалогового окна **Параметры** приложения.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[кмфкриббонкуиккакцесстулбардефаултстате](../../mfc/reference/cmfcribbonquickaccesstoolbardefaultstate-class.md)

## <a name="example"></a>Пример

В следующем примере показано, как создать объект `CMFCRibbonQuickAccessToolbarDefaultState` класса и добавить команду в состояние по умолчанию для панели быстрого доступа.

[!code-cpp[NVC_MFC_RibbonApp#21](../../mfc/reference/codesnippet/cpp/cmfcribbonquickaccesstoolbardefaultstate-class_1.cpp)]

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонкуиккакцесстулбар. h

## <a name="cmfcribbonquickaccesstoolbardefaultstateaddcommand"></a><a name="addcommand"></a> Кмфкриббонкуиккакцесстулбардефаултстате:: AddCommand

Добавляет команду в состояние по умолчанию для панели быстрого доступа.

```cpp
void AddCommand(
    UINT uiCmd,
    BOOL bIsVisible=TRUE);
```

### <a name="parameters"></a>Параметры

*[in] Уикмд*<br/>
Указывает идентификатор команды.

*[in] Бисвисибле*<br/>
Задает видимость команды, если панель быстрого доступа находится в состоянии по умолчанию.

### <a name="remarks"></a>Комментарии

Добавление команды в Кмфкриббонкуиккакцесстулбардефаултстате позволяет выполнить три результата. Во-первых, каждая добавленная команда отображается в раскрывающемся списке в правой части панели инструментов быстрого доступа. Таким образом, пользователь может легко добавить или удалить эту команду на панели быстрого доступа. Во-вторых, панель быстрого доступа сбрасывается и отображает только те команды, которые отображаются в состоянии по умолчанию, когда пользователь нажимает кнопку **Сброс** в диалоговом окне **Настройка** . В-третьих, если вы не вызывали [CMFCRibbonBar:: сеткуиккакцесскоммандс](../../mfc/reference/cmfcribbonbar-class.md#setquickaccesscommands), панель быстрого доступа использует видимые команды из этого списка в качестве видимых команд по умолчанию при первом запуске приложения пользователем. После добавления всех нужных команд вызовите [CMFCRibbonBar:: сеткуиккакцессдефаултстате](../../mfc/reference/cmfcribbonbar-class.md#setquickaccessdefaultstate) , чтобы установить этот экземпляр в качестве состояния по умолчанию для панели быстрого доступа этой ленты.

## <a name="cmfcribbonquickaccesstoolbardefaultstatecopyfrom"></a><a name="copyfrom"></a> Кмфкриббонкуиккакцесстулбардефаултстате:: CopyFrom

Копирует свойства одной панели быстрого доступа в другую.

```cpp
void CopyFrom(const CMFCRibbonQuickAccessToolBarDefaultState& src);
```

### <a name="parameters"></a>Параметры

*src*<br/>
окне Ссылка на исходный объект, `CMFCRibbonQuickAccessToolBarDefaultState` из которого необходимо выполнить копирование.

### <a name="remarks"></a>Комментарии

Этот метод копирует каждую команду из исходного `CMFCRibbonQuickAccessToolBarDefaultState` объекта в этот объект с помощью метода [кмфкриббонкуиккакцесстулбардефаултстате:: AddCommand](#addcommand) .

## <a name="cmfcribbonquickaccesstoolbardefaultstatecmfcribbonquickaccesstoolbardefaultstate"></a><a name="cmfcribbonquickaccesstoolbardefaultstate"></a> Кмфкриббонкуиккакцесстулбардефаултстате:: Кмфкриббонкуиккакцесстулбардефаултстате

Конструирует объект состояния панели быстрого доступа по умолчанию.

```
CMFCRibbonQuickAccessToolBarDefaultState();
```

### <a name="remarks"></a>Комментарии

По умолчанию список команд, содержащихся в новом экземпляре [кмфриббонкуиккакцесстулбардефаултстате](../../mfc/reference/cmfcribbonquickaccesstoolbardefaultstate-class.md) , пуст.

## <a name="cmfcribbonquickaccesstoolbardefaultstateremoveall"></a><a name="removeall"></a> Кмфкриббонкуиккакцесстулбардефаултстате:: RemoveAll

Очищает список команд по умолчанию на панели инструментов быстрого доступа.

```cpp
void RemoveAll();
```

### <a name="remarks"></a>Комментарии

Эта функция удаляет из этого экземпляра все команды, которые были добавлены предыдущими вызовами [кмфкриббонкуиккакцесстулбардефаултстате:: AddCommand](#addcommand) .

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md)
